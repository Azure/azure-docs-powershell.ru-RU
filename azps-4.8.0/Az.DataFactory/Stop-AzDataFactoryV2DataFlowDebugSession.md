---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242832"
---
# <span data-ttu-id="0837d-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0837d-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="0837d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0837d-102">SYNOPSIS</span></span>
<span data-ttu-id="0837d-103">Остановка сеанса отладки потока данных в фабрике данных Azure</span><span class="sxs-lookup"><span data-stu-id="0837d-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="0837d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0837d-104">SYNTAX</span></span>

### <span data-ttu-id="0837d-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0837d-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0837d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0837d-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0837d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0837d-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0837d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0837d-108">DESCRIPTION</span></span>
<span data-ttu-id="0837d-109">Эта команда останавливает сеанс отладки, в противном случае сеанс автоматически отключается в соответствии с настройками времени сеанса отладки в течение срока жизни.</span><span class="sxs-lookup"><span data-stu-id="0837d-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="0837d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0837d-110">EXAMPLES</span></span>

### <span data-ttu-id="0837d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0837d-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="0837d-112">Остановка сеанса отладки потока данных "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" в фабрике данных "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="0837d-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="0837d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0837d-113">PARAMETERS</span></span>

### <span data-ttu-id="0837d-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="0837d-114">-DataFactory</span></span>
<span data-ttu-id="0837d-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0837d-115">The data factory object.</span></span>

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

### <span data-ttu-id="0837d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0837d-116">-DataFactoryName</span></span>
<span data-ttu-id="0837d-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0837d-117">The data factory name.</span></span>

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

### <span data-ttu-id="0837d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0837d-118">-DefaultProfile</span></span>
<span data-ttu-id="0837d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0837d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0837d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0837d-120">-PassThru</span></span>
<span data-ttu-id="0837d-121">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="0837d-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0837d-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0837d-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="0837d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0837d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0837d-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0837d-124">The resource group name.</span></span>

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

### <span data-ttu-id="0837d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0837d-125">-ResourceId</span></span>
<span data-ttu-id="0837d-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0837d-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0837d-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="0837d-127">-SessionId</span></span>
<span data-ttu-id="0837d-128">Идентификатор сеанса отладки потока данных.</span><span class="sxs-lookup"><span data-stu-id="0837d-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="0837d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0837d-129">-Confirm</span></span>
<span data-ttu-id="0837d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0837d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0837d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0837d-131">-WhatIf</span></span>
<span data-ttu-id="0837d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0837d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0837d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0837d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0837d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0837d-134">CommonParameters</span></span>
<span data-ttu-id="0837d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0837d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0837d-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0837d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0837d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0837d-137">INPUTS</span></span>

### <span data-ttu-id="0837d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0837d-138">System.String</span></span>

### <span data-ttu-id="0837d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0837d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0837d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0837d-140">OUTPUTS</span></span>

### <span data-ttu-id="0837d-141">System. void</span><span class="sxs-lookup"><span data-stu-id="0837d-141">System.Void</span></span>

### <span data-ttu-id="0837d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0837d-142">System.Boolean</span></span>

## <span data-ttu-id="0837d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0837d-143">NOTES</span></span>
<span data-ttu-id="0837d-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="0837d-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0837d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0837d-145">RELATED LINKS</span></span>

[<span data-ttu-id="0837d-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0837d-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="0837d-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="0837d-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="0837d-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="0837d-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="0837d-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="0837d-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)