# 프란틀수 계산기

운동량 확산과 열확산의 비율인 프란틀수 계산

- Plan ID: E072
- App: https://nanalab.kr/eng-prandtl-number/
- Repository: https://github.com/NaNaCompany/eng-prandtl-number
- Formula: `Pr = μc_p/k`
- Output: 프란틀수 Pr

## Model

μ,c_p,k>0. 동일 유체·온도·압력의 물성을 사용한다. 점성계수 μ를 동점성계수 ν로 대신 넣지 않는다. 비뉴턴 유체의 유효 물성을 자동 추정하지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `7`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
