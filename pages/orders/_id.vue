<template>
<div>
  <div class="card my-2 p-4">
      <h4>My Orders</h4>
      <h5>Next step for this order</h5>
      <p>once your have delivered  the order please mark the status as delivered and upload you proof of delivery</p>
  </div>
  <div class="card my-2 p-4">
    <div class="flex gap-4">
      <div>
        <p>Order Number:</p>
        <p><strong>2323232112312</strong></p>
      </div>
      <div>
        <p>Initial Date:</p>
        <p><strong>12-nov-24 4:44pm</strong></p>
      </div>
      <div>
        <p>Delivery Method:</p>
        <p><strong>EX Works</strong></p>
      </div>
      <div>
        <p>Order Status</p>
        <p class="text-warning p-1 rounded bg-smooth">Ready To Ship</p>
      </div>
      <div>
        <p>Invoice Status</p>
        <p class="text-warning p-1 rounded bg-smooth">Pending Upload</p>
      </div>
      <div>
        <p>Pickup Date</p>
        <p><strong>10 jan 24</strong></p>
      </div>
      <div>
        <p>Pickup Location</p>
        <p><strong class="flex gap-2"><svg class="w-6 h-6 text-gray" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 13a3 3 0 1 0 0-6 3 3 0 0 0 0 6Z"/>
    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.8 14h0a7 7 0 1 0-11.5 0h0l.1.3.3.3L12 21l5.1-6.2.6-.7.1-.2Z"/>
  </svg> <span>Office</span></strong></p>
      </div>
    </div>
  </div>
  <div class="card my-2 p-4">
    <h4>Orders overview</h4>
    <!-- component -->
<!-- This is an example component -->
<div class='flex w-full from-purple-200 via-purple-300 to-purple-500 bg-gradient-to-br'>
    <div class="flex items-center w-full justify-between">
            <div class="relative w-full">
            <table class="w-full text-sm text-left text-gray-500 ">
                <thead class="text-xs  uppercase bg-gray-50  ">
                <tr>
                    <th scope="col" class="py-3 px-6">Product</th>
                    <th scope="col" class="py-3 px-6">Agreed Price</th>
                    <th scope="col" class="py-3 px-6">Quantity</th>
                    <th scope="col" class="py-3 px-6">Item Status</th>
                    <th scope="col" class="py-3 px-6">Subtotal</th>
                    <th scope="col" class="py-3 px-6">Commission %</th>
                    <th scope="col" class="py-3 px-6">Commission Subtotal</th>
                </tr>
                </thead>
                <tbody>
                <tr class="bg-white">
                    <td class="py-4 px-6"> 
                      <div class="flex gap-2">
                        <img src="https://c8n.tradeling.com/img/plain/cms/rs:auto:600::0/f:webp/q:95/Apple_f92d899cac.png" alt="">
                        <div>
                          <p class="font-bold">Product name here ...</p>
                          <p><del>321321</del></p>
                          <p>MCQ:3</p>
                          <p>SKU: QF-1</p>
                        </div>
                      </div>
                    </td>
                    <td class="py-4 px-6">SAR 82926417</td>
                    <td class="py-4 px-6">10</td>
                    <td class="py-4 px-6"><span class="bg-smooth text-warning p-2 rounded">Cancel</span></td>
                    <td class="py-4 px-6"><del>$4,500.00</del></td>
                    <td class="py-4 px-6">20%</td>
                    <td class="py-4 px-6"><del>$4,500.00</del></td>
                </tr>
                <tr class="bg-white">
                    <td class="py-4 px-6"> 
                      <div class="flex gap-2">
                        <img src="https://c8n.tradeling.com/img/plain/cms/rs:auto:600::0/f:webp/q:95/Apple_f92d899cac.png" alt="">
                        <div>
                          <p class="font-bold">Product name here ...</p>
                          <p><del>321321</del></p>
                          <p>MCQ:3</p>
                          <p>SKU: QF-1</p>
                        </div>
                      </div>
                    </td>
                    <td class="py-4 px-6">SAR 82926417</td>
                    <td class="py-4 px-6">10</td>
                    <td class="py-4 px-6"><span class="bg-smooth text-primary p-2 rounded">Iteams Placed</span></td>
                    <td class="py-4 px-6">$4,500.00</td>
                    <td class="py-4 px-6">20%</td>
                    <td class="py-4 px-6">$4,500.00</td>
                </tr>
                </tbody>
            </table>
            </div>
    
</div>
</div>
<!-- ------------subtotal--------------- -->
<div class="w-full">
                              <div class="w-1/4 ml-auto items-end border border-smooth p-4 rounded">
                              <div class="flex my-1 justify-between">
                                  <div><h5>Item(S) Subtotal</h5></div>
                                  <div><h5>SAR 123343</h5></div>
                              </div>
                              <div class="flex my-1 justify-between">
                                  <div><h5>Vat (%):</h5></div>
                                  <div><h5>SAR 123343</h5></div>
                              </div>
                              <div class="flex my-1 justify-between">
                                  <div><h5>Item(S) Total</h5></div>
                                  <div><h5>SAR 123343</h5></div>
                              </div>
                              <div class="flex my-2 justify-between">
                                  <div><h5 class="font-bold">Industry fee</h5></div>
                              </div>
                              <div class="flex my-1 justify-between">
                                  <div><h5>Commission</h5></div>
                                  <div><h5>SAR 1233</h5></div>
                              </div>
                              <div class="flex my-1 justify-between">
                                  <div><h5>VAT(S) on Comission (5%)</h5></div>
                                  <div><h5>SAR 123343</h5></div>
                              </div>
                              <div class="flex my-1 justify-between">
                                  <div><h5>Total Comission</h5></div>
                                  <div><h5>SAR 123343</h5></div>
                              </div>
                              <div class="flex border-t border-smooth pt-2 my-1 justify-between">
                                  <div><h5  class="font-bold">Total Payout</h5></div>
                                  <div><h5  class="font-bold">SAR 123343</h5></div>
                              </div>
                            </div>
                            </div>
  </div>
  <div class="card my-2 p-4">
    <div>
      <div>
       <div class="title border-b border-smooth">
        <h4>Payment Shipping & Dimenssion</h4>
       </div>
       <div class="card w-1/4 my-2 p-4">
        <p class="flex gap-4">Payment Method: <strong  class="flex gap-4">Visa *****002 <img class="w-10 leading-3 rounded shadow object-cover mt-1 p-1 h-5" src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5OjcBCgoKDQwNGg8PGjclHyU3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3N//AABEIAKgAswMBIgACEQEDEQH/xAAcAAEAAwEAAwEAAAAAAAAAAAAABgcIBQIDBAH/xABCEAABAwMBAwkEBQsEAwAAAAABAAIDBAURBgcSIRMUMUFRYXGBkRUiVaEWMkKCkyNSU3KSlKKxssHRYsLw8TNDc//EABoBAQACAwEAAAAAAAAAAAAAAAADBAECBQb/xAAyEQACAgIAAwUFBwUAAAAAAAAAAQIDBBEFEjEhQVFxsRMUImHxMoGRocHR4RUjQlLw/9oADAMBAAIRAxEAPwC8UREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAEREAREQBERAcH6aaY+O2/8AHan000x8dt/47VU2rdm9zsFPJW0sra+hjG89zW7skbe0t6wO0HyAUJXoaeFYt0eauxtFSV84vTRqO33GiucHL26rgqos434ZA8A9nBfUs67PbvNZ9WUD45C2GplbTztzwe1xwM+BIP8A2tFLmZ+H7rYop7TJqrPaLYXx3O6UFphbNc6yGlie7ca+Z4aC7BOOPcCvsVJbZbzz7UEVsidmKgZ7+OuR4BPo3d9StMLF95uUO7vM2T5I7LP+mmmPjtv/AB2r67ZqCz3ad0FsuVNVStbvuZDIHENzjPDxCzKrs2NWTmNglukzMTXB2W56om5DfU7x8MLoZvDacalz5nvuIqrpTlrRMbpe7VaHRtudwpqR0gJYJpA0uA6cZ8Qvi+memfj1v/eGqqNsddzrV/NmnLaOnZGR2Od75+TmqCqTG4PC2mM5SabNZ5DjJpI1HbbnQ3WAz22rhqoWu3C+F4cA7pxkeIX1qK7L6LmWiLcCPena6d3fvkkfw4XP2ia8bpzFvtrWS3N7d5xdxbA09BI63HqHmeoHle6ynkOmrt7f+ZPzpQ5pEyrq6kt8Bnr6qGmiH25pAwepUaqtpGlKZxb7T5Uj9DC949QMKh7jX1lzqjVXGplqZz/7JXZI7h2DuHBfOu3VwOtL+5Jt/IrSyn3IvuLafpSR2HV00fe+mkx8gu/a9Q2a7nFtudLUP6dxkg3x93pWZV3NDUAuOsLRTubloqRKeHUwF/8AtWL+DURg5Rk1pb8f2MxyJN6aNIoiLzZcPTV1VPRwPqKyeKCFnF0krw1rfElcj6ZaZ+PW794aqj2r35131LJRxyF1HbzybGg+6Zftu8fs+XeVCl38bg0Z1KdkmmyrPJ1LSRpak1TYK2pjpqS8UU08hwyNkzS5x7AF2Fl20Vvs27UVdnApqhkpx2NcCfllahBBGQcgqjxHBWLKPK9pklNvtE9n6iIucTHjJGyWN0cjQ5jwWuB6wVl660TrbdKygeDmmnfFx6w1xAPmOK1GqH2vW7mWsZJ2jDK2Fk2ereHun+kHzXb4Jby2yr8V6FbJjuKZC2yPhc2WI7skZD2HsI4hanpJ2VVJDUR/Umja9vgRlZXWiNm9Zz3RNqfnJji5E/cJb/IBWeOQ3XCfg9fj9DTFfa0dq7V8NrtlVX1J/JU0TpHY6TgZwO9ZjraqaurJ6ypOZp5HSSHvcclW7trvPN7VS2eJ3v1b+Ulx+jYRgebsfslU4pODUclTsfWXojXJnuXL4H22W2y3i70dtgyH1MoZkfZHS53kAT5LTdJTRUdLDS07AyGFjY42joa0DAHoqo2JWXlKisvczfdjHN4M/nHBefTdHmVZeo672ZYLjXD61PTSPb3uDTgeuFR4vc7r1THu9WS48eWHMzO2qa72lqS6VmctlqX7h/0g7rfkAubHG+aRkMQzJI4MYO0k4C8QMADpUg0DRe0NZ2mAty1s/Ku8GAv/AJtC9FJqmpvuivQpr4peZoOCOG1WmOJoxBSU4aAOprG/4CzLca6a519RX1JzNUyGR/dnq8B0eS07cKfndBU02cctE6PPZkELLksMlPK+CdhZLE4skaelrgcEeq4nA9N2SfXs/UtZXcjzpKeSrq4KWHHKzytiZvHA3nEAZ8yrttOyvT1JTsFwZNX1GPfe+VzG57mtI4eOVRzXOa4OY4tc05DgcEHtCtfSW1aPk46TUzHNeAGitibkO73tHEHvGfAK5xOGU4J0Pz11IqHDfxEjqdmOlJ2kMoZoHH7UVTJw8nEj5L06V2eQaa1EblBXPqIOQdGyOVg32OJHHeHA8AR0DpUxo6umrqZlTRTxzwPGWyRuDmnzC96848zJ5XCU3p9d/wAlz2cN7SC4+rby2waerbiccpHHiJp+1IeDR6kLsKnttl75eupLJC7LKccvOB+eRho8m5P3gs4OP7e+MO7v8hbPki2VmS5xLnuLnE5c5xySeslfpa4MDy07pJAdjgSMZHzHqF4k4GT0BWFrHTPsnZ5p+V0ZbUxykz56QZm7xB8C1rfJewtujXKEX/k9fkc+MW034FekZBB61pXRtcblpW1Vbjl76Zgef9QGHfMFZrV37F67nGlJKV3TSVT2D9V2H59XO9FzeNV81Cl4P1JsZ6lonyIi8sXgq024W7lbTb7k0e9TTGJxH5rx1+bR6qy1wddW72ppG6UrW70nIGSMdr2e835gK1hW+yyIT+f8GlkeaDRnBXNsQrDLp+upHOyaeq3mjsa5o/uHKmAcjIUj0pqN9goL6yJxbNWUrY4SOp+9jPk17j5L1XEKHfQ4R69nqUKZcsts9eurz7d1TW1jHb0DHcjB2bjOAI8Tl3muExj5HtjiYXyPIaxjelxPAALxAwMDoU22S2T2rqhtXK3NPb28s7sMh4MH83fdUs5QxaN90UapOcvMuPS9oZYbBRW1mC6GMco4faeeLj5klR3bBXc00bJCDh1XPHCPDO+fk35qbqo9uddvVVqt7XcGMfO9viQ1p+T15bAi7syLl47/AFL9r5a3oq5WLsRouW1BXVpHCmpgweL3f4YVXSurYnRGDTdVWOHGqqjunta0Af1by9BxSzkxZfPsKdC3NFhqutouz514lfdrIGtryPy0BOBPjrB6nfI9ysVF5XHyLMefPB9pfnBTWmZWqaeekqH09VDJDPGcPjkaWub4gr1rTN+09atQQcjdaNk2B7kn1Xs/VcOIVIa90bLpSridHKZ6CoJEMjh7zSPsuxwz3jp48Bheow+J15L5GtSKNlDh29xy9N6juWm6wVFtnIaT+VgccxyjvHb39IWgtMX6l1HaIrjR5aHe7JGTkxPHS0/84gg9azOrR2GVMgqrtSZJiLI5QOoOyQT5jHoouL4sJ0u5L4l+Ztj2NS5e4tWuq4aCinrKl+5BBG6SR3Y0DJWY7tcJrtdKq41P/lqZTIR+bnoHkMDyVvbZ73zOywWmF2Ja529JjqiYQT6u3fIFUutOC4/JW7X1fp9TOTPb5Tu6HtHtvVVBRubvQiTlZuHDcZxOe4nDfvK6tpVFz7RF1Z1xRcuO7cIcfkCqm2e6ot2laisqa2kqaieZrY4zDu4Y3pPSR0nHoplVbWrLU00tPLargWSsLHD8nxBGD9pa59eTZlRnCO1HX7manBQab6lPqy9h1byd2uVA48JoGytHew4P9Y9FWYGABnOFJ9mlaaHW1sdvYZM90D+8OaQB+1urpZ1ftMacfl6dpBU9TTNDoiLxJ0whAIwehEQGYdQ2/wBlX24UGMNp6h7GfqZy3+EhfAp5tlt3NNVsrGtw2uga4ntez3T8txQNe6xbfa0xn4o5c48smj8WgNl1k9jaUgdKzdqa084lz0gH6o8m44dpKprRllN/1LRUDm5hL+Un/wDk3i714N+8tJAADAGAFx+N5GlGleb/AELGNDrI/Vn7anW891vXYOW07WQN8hk/xOctAPc1jHPccNaMk9gWWrhVmvuFXWnpqZ3zftOLv7qHgde7JT8F6/Q2yn8KR854DK0hoSh9naQtNOW7r+btkeOxz/ePzcVni3UZuFwpaFuc1MzIcjq3nAZ+a1IxoY0NaMNaMAdgU/HLPhhD7zXFXa2QHXevqnS+oKWip6aGphNPys7HOLXcXEDDur6p6j0hey37V9OVDAavndE/rEkJePIsyqy2k1jqzW90LsjkniJjXDBw1oHpnJ81GlLVwqiyiHMtPXVGsr5qT0X/AC7StJxs3hc3PPU1tNLk/wAKrHaJrRuqpqeCkgfDQ0zi5vKY35HHhkgdAAzgd5UOX4SAMkgDvVjG4ZRRPnjtv5mk75TWmfqt/Yha5IbfcLrK0htS9sUWetrM5I83Y+6olo7Z9c7/ADRz1sclFbel0jxuvkHYwH+o8PFWXr24QaV0S+ntzWwOewUlKxnDdyOJHg0OOe1VuI5MbdYtT25Pt+RJTBx+OXcVDru9+39UVlYx29TsdyNP2cm3IBHicu81H0AwMBSzZjZWXnVkDZ4xJTUrTPK1zctdjg0H7xBx3FdOThjU77oog7Zy8yJ7w7Qm8O0LT3sO0fCqH92Z/hPYdo+FUP7sz/C5P9dh/o/xLHur8TMIOehe6kqXUVXBVx/Xp5Wyt8WkEfyU+2zWmnt92t1TSU8UEU8DmFsTA1u8x2c4HXh/yVdrrUXRyKlYl2Mrzi4S0arhkbNEyWM5Y9oc09oKKObP7nFV6MtEkkrQ9lOInbx45YSz/ai8TZW4TcPB6OmntbJMiIozJz7rZLXeOS9qUMFVyWeT5Vmd3OM49B6Ln/QnTHwOh/CCkCKSN1kVqMml5mHFPqjmWvT9otEz5rZbqelke3dc6JmCR04XTRFrKUpPcnsJJdDwmiZNE+KVodG9pa5p6wekLg/QfS/wOi/DUhRZhbOH2W0Gk+pxKTSOnqKpjqaW0UkU8Tt5kjWcWntC7aIsTnKb3J7CSXQ+S4WygucfJ3Gip6pnUJog/Hqo9U7ONKVDi42sRk/oZpGD0BwpYi3hfbX9iTXkzDjF9UQxmy/SjXZNHO/udVSf2K7Vr0pYLS9slBaqWKRvRIWbzx945K7KLaeVfNalNv7woRXRBc+7WS2XkRC6UUNUIs7glGd3PTj0C6CKGMnF7i9M2a2R76EaX+B0X4a6FpsVqsxlNroIKUy4EhibjexnGfUroopJXWyWpSbXmYUUuiCIiiMnwXWzW28MjZdKKGqbGSWCVud0nsXN+hGl/gdF+GpCikjdZFajJpeZhxT6o5dPp60UsLYaagiiibnDGZAGTlF1EWHZN97GkERFoZCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiIAiIgCIiAIiID/2Q==" alt=""></strong></p>
        <p>Shipping Method: <strong>Ex Works</strong></p>
        <p>Shipping Cost: <strong class="text-primary">N/A</strong></p>
      </div>
      </div>
    </div>
  </div>
  <div class="card p-4">
    <div>
      <h4>Timeline</h4>
    </div>
    <!-- component -->
<!-- This is an example component -->
<div class='flex w-full from-purple-200 via-purple-300 to-purple-500 bg-gradient-to-br'>
    <div class="flex w-full items-center justify-center">
        <div class="overflow-x-auto w-full relative sm:rounded-lg">
            <div class="overflow-x-auto w-full relative sm:rounded-lg">
            <table class="w-full text-sm text-left text-gray-500 ">
                <thead class="text-xs  uppercase bg-gray-50  ">
                <tr>
                    <th scope="col" class="py-3 px-6">User</th>
                    <th scope="col" class="py-3 px-6">Action</th>
                    <th scope="col" class="py-3 px-6">Date</th>
                </tr>
                </thead>
                <tbody>
                <tr class="bg-white">
                    <td class="py-4 px-6">Buyer</td>
                    <td class="py-4 px-6">item placed</td>
                    <td class="py-4 px-6">Nov 09, 23 4:55pm</td>
                </tr>
                <tr class="bg-white">
                    <td class="py-4 px-6">System</td>
                    <td class="py-4 px-6">order status changed</td>
                    <td class="py-4 px-6">Nov 09, 23 4:55pm</td>
                </tr>
                <tr class="bg-white">
                    <td class="py-4 px-6">Suplier</td>
                    <td class="py-4 px-6">item placed</td>
                    <td class="py-4 px-6">Nov 09, 23 4:55pm</td>
                </tr>
                <tr class="bg-white">
                    <td class="py-4 px-6">Buyer</td>
                    <td class="py-4 px-6">item placed</td>
                    <td class="py-4 px-6">Nov 09, 23 4:55pm</td>
                </tr>
                </tbody>
            </table>
            </div>
    </div>
    
</div>
</div>

  </div>
</div>
</template>