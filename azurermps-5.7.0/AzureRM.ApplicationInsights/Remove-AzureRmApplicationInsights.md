---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733592"
---
# <span data-ttu-id="fe628-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fe628-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="fe628-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe628-102">SYNOPSIS</span></span>
<span data-ttu-id="fe628-103">Удаление ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="fe628-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe628-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe628-104">SYNTAX</span></span>

### <span data-ttu-id="fe628-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe628-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe628-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe628-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe628-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe628-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe628-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe628-108">DESCRIPTION</span></span>
<span data-ttu-id="fe628-109">Удаление ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="fe628-109">Remove an application insights resource</span></span>

## <span data-ttu-id="fe628-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe628-110">EXAMPLES</span></span>

### <span data-ttu-id="fe628-111">Пример 1. Удалите ресурс Application Insights</span><span class="sxs-lookup"><span data-stu-id="fe628-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="fe628-112">Удаление ресурса Insights applciation с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="fe628-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="fe628-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe628-113">PARAMETERS</span></span>

### <span data-ttu-id="fe628-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="fe628-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="fe628-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fe628-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe628-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe628-116">-Confirm</span></span>
<span data-ttu-id="fe628-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe628-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe628-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe628-118">-DefaultProfile</span></span>
<span data-ttu-id="fe628-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe628-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe628-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe628-120">-Name</span></span>
<span data-ttu-id="fe628-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fe628-121">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe628-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe628-122">-PassThru</span></span>
<span data-ttu-id="fe628-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="fe628-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="fe628-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fe628-124">This parameter is optional.</span></span> <span data-ttu-id="fe628-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="fe628-125">Default value is false.</span></span>

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

### <span data-ttu-id="fe628-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe628-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe628-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe628-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe628-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe628-128">-ResourceId</span></span>
<span data-ttu-id="fe628-129">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="fe628-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe628-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe628-130">-WhatIf</span></span>
<span data-ttu-id="fe628-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe628-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe628-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe628-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe628-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe628-133">CommonParameters</span></span>
<span data-ttu-id="fe628-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe628-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe628-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe628-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe628-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe628-136">INPUTS</span></span>

### <span data-ttu-id="fe628-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fe628-137">System.String</span></span>

## <span data-ttu-id="fe628-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe628-138">OUTPUTS</span></span>

### <span data-ttu-id="fe628-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="fe628-139">System.Object</span></span>

## <span data-ttu-id="fe628-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe628-140">NOTES</span></span>

## <span data-ttu-id="fe628-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe628-141">RELATED LINKS</span></span>

