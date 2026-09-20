# Accessibility Baseline & Repository Architecture Audit

## 1. Audit target

**Website:** DigiLocker public sign-up/login page\
**Audit method:** Chrome Lighthouse accessibility audit + planned
keyboard-only navigation pass\
**Lighthouse evidence:** Accessibility score **71/100** in the captured
run.

> Important: the Lighthouse score is directly evidenced by the supplied
> screenshot. The five issue records below are audit items to verify
> with the browser accessibility tree and keyboard pass; they are not
> all claimed as Lighthouse-detected failures.

## 2. Findings

  ------------------------------------------------------------------------------------
  ID             Issue                 WCAG           Priority       Evidence /
                                                                     verification
  -------------- --------------------- -------------- -------------- -----------------
  WEB-001        Mobile-number input   3.3.2          High           Inspect the input
                 needs an explicit                                   in the
                 programmatic                                        Accessibility
                 label/instruction                                   tree and record
                                                                     its accessible
                                                                     name.

  WEB-002        Date-of-Birth         3.3.2          Medium         Inspect
                 controls need clear                                 date/month/year
                 labels/instructions                                 controls and
                                                                     verify their
                                                                     accessible names
                                                                     and grouping.

  WEB-003        Mobile-number         3.3.1          High           Trigger invalid
                 validation needs                                    input and verify
                 programmatic                                        that the error is
                 association                                         associated with
                                                                     and announced for
                                                                     the field.

  WEB-004        Keyboard              2.1.1          High           Navigate with
                 navigation/focus                                    Tab/Shift+Tab
                 needs verification                                  only and capture
                                                                     any skipped
                                                                     control or
                                                                     missing visible
                                                                     focus.

  WEB-005        QR-login graphic/flow 1.1.1          Medium         Inspect the QR
                 needs accessible                                    graphic's
                 text/equivalent path                                accessible name
                                                                     and verify an
                                                                     equivalent
                                                                     non-visual route.
  ------------------------------------------------------------------------------------

## 3. Lighthouse evidence

The captured Lighthouse run reports:

-   Performance: 58
-   Accessibility: **71**
-   Best Practices: 81
-   SEO: 82

The screenshot is stored at
`docs/screenshots/lighthouse-accessibility-71.png`.

## 4. Keyboard-only test procedure

1.  Reload the page.
2.  Do not use the mouse.
3.  Press `Tab` repeatedly through every interactive element.
4.  Use `Shift+Tab` to move backwards.
5.  Record whether every control is reachable, whether the order is
    logical, and whether focus is visible.
6.  Test activation with Enter/Space where applicable.
7.  Save screenshots for any reproducible failure.

## 5. Remediation priority

**High:** issues that can prevent form completion, keyboard operation,
or understanding validation errors.

**Medium:** issues that reduce the accessibility of non-text content or
make form controls harder to understand.

## 6. Evidence policy

Do not label an issue as a confirmed Lighthouse failure unless the
Lighthouse report explicitly identifies it. Use the Lighthouse score as
baseline evidence and use the Accessibility tree/keyboard pass for the
individual issue evidence.
