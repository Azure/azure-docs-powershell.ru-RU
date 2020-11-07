---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: def0ff5b525f4ced0ac1510fdc65b1dfd746cc6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721424"
---
# <span data-ttu-id="3fa8e-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3fa8e-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="3fa8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fa8e-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa8e-103">Остановка сеанса отладки потока данных в фабрике данных Azure</span><span class="sxs-lookup"><span data-stu-id="3fa8e-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="3fa8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fa8e-104">SYNTAX</span></span>

### <span data-ttu-id="3fa8e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3fa8e-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fa8e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3fa8e-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa8e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa8e-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa8e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fa8e-108">DESCRIPTION</span></span>
<span data-ttu-id="3fa8e-109">Эта команда останавливает сеанс отладки, в противном случае сеанс автоматически отключается в соответствии с настройками времени сеанса отладки в течение срока жизни.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="3fa8e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fa8e-110">EXAMPLES</span></span>

### <span data-ttu-id="3fa8e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3fa8e-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="3fa8e-112">Остановка сеанса отладки потока данных "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" в фабрике данных "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="3fa8e-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="3fa8e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fa8e-113">PARAMETERS</span></span>

### <span data-ttu-id="3fa8e-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-114">-DataFactory</span></span>
<span data-ttu-id="3fa8e-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8e-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3fa8e-116">-DataFactoryName</span></span>
<span data-ttu-id="3fa8e-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa8e-118">-DefaultProfile</span></span>
<span data-ttu-id="3fa8e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fa8e-120">-PassThru</span></span>
<span data-ttu-id="3fa8e-121">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="3fa8e-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="3fa8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="3fa8e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa8e-125">-ResourceId</span></span>
<span data-ttu-id="3fa8e-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8e-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="3fa8e-127">-SessionId</span></span>
<span data-ttu-id="3fa8e-128">Идентификатор сеанса отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa8e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fa8e-129">-Confirm</span></span>
<span data-ttu-id="3fa8e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa8e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa8e-131">-WhatIf</span></span>
<span data-ttu-id="3fa8e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa8e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa8e-134">CommonParameters</span></span>
<span data-ttu-id="3fa8e-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fa8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa8e-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fa8e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa8e-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fa8e-137">INPUTS</span></span>

### <span data-ttu-id="3fa8e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3fa8e-138">System.String</span></span>

### <span data-ttu-id="3fa8e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3fa8e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3fa8e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fa8e-140">OUTPUTS</span></span>

### <span data-ttu-id="3fa8e-141">System. void</span><span class="sxs-lookup"><span data-stu-id="3fa8e-141">System.Void</span></span>

### <span data-ttu-id="3fa8e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fa8e-142">System.Boolean</span></span>

## <span data-ttu-id="3fa8e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fa8e-143">NOTES</span></span>
<span data-ttu-id="3fa8e-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3fa8e-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3fa8e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fa8e-145">RELATED LINKS</span></span>

[<span data-ttu-id="3fa8e-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3fa8e-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3fa8e-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3fa8e-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="3fa8e-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="3fa8e-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="3fa8e-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="3fa8e-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)