---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911114"
---
# <span data-ttu-id="cc9c4-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cc9c4-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="cc9c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9c4-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="cc9c4-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="cc9c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc9c4-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc9c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cc9c4-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="cc9c4-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="cc9c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc9c4-107">EXAMPLES</span></span>

### <span data-ttu-id="cc9c4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc9c4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cc9c4-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="cc9c4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cc9c4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc9c4-110">PARAMETERS</span></span>

### <span data-ttu-id="cc9c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9c4-111">-DefaultProfile</span></span>
<span data-ttu-id="cc9c4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cc9c4-113">-Force</span></span>
<span data-ttu-id="cc9c4-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc9c4-115">-Name</span></span>
<span data-ttu-id="cc9c4-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc9c4-117">-PassThru</span></span>
<span data-ttu-id="cc9c4-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="cc9c4-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc9c4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc9c4-121">-Confirm</span></span>
<span data-ttu-id="cc9c4-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9c4-123">-WhatIf</span></span>
<span data-ttu-id="cc9c4-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9c4-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc9c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9c4-126">CommonParameters</span></span>
<span data-ttu-id="cc9c4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc9c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9c4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc9c4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9c4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc9c4-129">INPUTS</span></span>

### <span data-ttu-id="cc9c4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cc9c4-130">System.String</span></span>

## <span data-ttu-id="cc9c4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc9c4-131">OUTPUTS</span></span>

### <span data-ttu-id="cc9c4-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="cc9c4-132">System.Object</span></span>

## <span data-ttu-id="cc9c4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc9c4-133">NOTES</span></span>

## <span data-ttu-id="cc9c4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc9c4-134">RELATED LINKS</span></span>

