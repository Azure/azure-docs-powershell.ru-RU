---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235172"
---
# <span data-ttu-id="bcdbd-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="bcdbd-101">Select-AzProfile</span></span>

## <span data-ttu-id="bcdbd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdbd-103">Для модулей, поддерживающих несколько профилей служб, загрузите командлеты, соответствующие заданному профилю службы.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="bcdbd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcdbd-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcdbd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcdbd-105">DESCRIPTION</span></span>
<span data-ttu-id="bcdbd-106">Для модулей, поддерживающих несколько профилей служб, загрузите командлеты, соответствующие заданному профилю службы.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="bcdbd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcdbd-107">EXAMPLES</span></span>

### <span data-ttu-id="bcdbd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bcdbd-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="bcdbd-109">Загрузка командлетов для профиля AzureStack из 2019 марта</span><span class="sxs-lookup"><span data-stu-id="bcdbd-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="bcdbd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcdbd-110">PARAMETERS</span></span>

### <span data-ttu-id="bcdbd-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcdbd-111">-Name</span></span>
<span data-ttu-id="bcdbd-112">Имя выбранного профиля.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdbd-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcdbd-113">-PassThru</span></span>
<span data-ttu-id="bcdbd-114">При обнаружении вызывает принудительное возвращение значения командлетом при успешном выполнении</span><span class="sxs-lookup"><span data-stu-id="bcdbd-114">When present, forces the cmdlet to return a value on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdbd-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcdbd-115">-Confirm</span></span>
<span data-ttu-id="bcdbd-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdbd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdbd-117">-WhatIf</span></span>
<span data-ttu-id="bcdbd-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdbd-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdbd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdbd-120">CommonParameters</span></span>
<span data-ttu-id="bcdbd-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcdbd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdbd-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcdbd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdbd-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcdbd-123">INPUTS</span></span>

### <span data-ttu-id="bcdbd-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="bcdbd-124">None</span></span>

## <span data-ttu-id="bcdbd-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcdbd-125">OUTPUTS</span></span>

### <span data-ttu-id="bcdbd-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="bcdbd-126">System.Object</span></span>
## <span data-ttu-id="bcdbd-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcdbd-127">NOTES</span></span>

## <span data-ttu-id="bcdbd-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcdbd-128">RELATED LINKS</span></span>
