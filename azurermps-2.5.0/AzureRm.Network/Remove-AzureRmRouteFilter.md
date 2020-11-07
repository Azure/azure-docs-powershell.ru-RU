---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915082"
---
# <span data-ttu-id="900ab-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="900ab-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="900ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="900ab-102">SYNOPSIS</span></span>
<span data-ttu-id="900ab-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="900ab-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="900ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="900ab-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="900ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="900ab-105">DESCRIPTION</span></span>
<span data-ttu-id="900ab-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="900ab-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="900ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="900ab-107">EXAMPLES</span></span>

### <span data-ttu-id="900ab-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="900ab-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="900ab-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="900ab-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="900ab-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="900ab-110">PARAMETERS</span></span>

### <span data-ttu-id="900ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900ab-111">-DefaultProfile</span></span>
<span data-ttu-id="900ab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="900ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="900ab-113">-Force</span><span class="sxs-lookup"><span data-stu-id="900ab-113">-Force</span></span>
<span data-ttu-id="900ab-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="900ab-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="900ab-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="900ab-115">-Name</span></span>
<span data-ttu-id="900ab-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="900ab-116">The resource name.</span></span>

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

### <span data-ttu-id="900ab-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="900ab-117">-PassThru</span></span>
<span data-ttu-id="900ab-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="900ab-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="900ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="900ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="900ab-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="900ab-120">The resource group name.</span></span>

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

### <span data-ttu-id="900ab-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="900ab-121">-Confirm</span></span>
<span data-ttu-id="900ab-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="900ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="900ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="900ab-123">-WhatIf</span></span>
<span data-ttu-id="900ab-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="900ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="900ab-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="900ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="900ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900ab-126">CommonParameters</span></span>
<span data-ttu-id="900ab-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="900ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900ab-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="900ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900ab-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="900ab-129">INPUTS</span></span>

### <span data-ttu-id="900ab-130">System. String</span><span class="sxs-lookup"><span data-stu-id="900ab-130">System.String</span></span>

## <span data-ttu-id="900ab-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="900ab-131">OUTPUTS</span></span>

### <span data-ttu-id="900ab-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="900ab-132">System.Object</span></span>

## <span data-ttu-id="900ab-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="900ab-133">NOTES</span></span>

## <span data-ttu-id="900ab-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="900ab-134">RELATED LINKS</span></span>

