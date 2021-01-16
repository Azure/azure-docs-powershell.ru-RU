---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407820"
---
# <span data-ttu-id="a5e44-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a5e44-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a5e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e44-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e44-103">Остановка сеанса отлагки потока данных в фабрике данных Azure</span><span class="sxs-lookup"><span data-stu-id="a5e44-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="a5e44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5e44-104">SYNTAX</span></span>

### <span data-ttu-id="a5e44-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5e44-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e44-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a5e44-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e44-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e44-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e44-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5e44-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e44-109">Эта команда останавливает сеанс отключки, если его нет, в соответствии с параметром Time To Live сеанса отключается автоматически.</span><span class="sxs-lookup"><span data-stu-id="a5e44-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="a5e44-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5e44-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e44-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5e44-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="a5e44-112">Остановка сеанса отладки потока данных "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" в фабрике данных "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="a5e44-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="a5e44-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5e44-113">PARAMETERS</span></span>

### <span data-ttu-id="a5e44-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a5e44-114">-DataFactory</span></span>
<span data-ttu-id="a5e44-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a5e44-115">The data factory object.</span></span>

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

### <span data-ttu-id="a5e44-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a5e44-116">-DataFactoryName</span></span>
<span data-ttu-id="a5e44-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a5e44-117">The data factory name.</span></span>

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

### <span data-ttu-id="a5e44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e44-118">-DefaultProfile</span></span>
<span data-ttu-id="a5e44-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e44-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5e44-120">-PassThru</span></span>
<span data-ttu-id="a5e44-121">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="a5e44-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a5e44-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a5e44-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5e44-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e44-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5e44-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5e44-124">The resource group name.</span></span>

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

### <span data-ttu-id="a5e44-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e44-125">-ResourceId</span></span>
<span data-ttu-id="a5e44-126">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e44-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a5e44-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="a5e44-127">-SessionId</span></span>
<span data-ttu-id="a5e44-128">ИД сеанса отлагки потоков данных.</span><span class="sxs-lookup"><span data-stu-id="a5e44-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="a5e44-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5e44-129">-Confirm</span></span>
<span data-ttu-id="a5e44-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e44-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e44-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e44-131">-WhatIf</span></span>
<span data-ttu-id="a5e44-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e44-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e44-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5e44-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e44-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e44-134">CommonParameters</span></span>
<span data-ttu-id="a5e44-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e44-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e44-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5e44-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e44-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5e44-137">INPUTS</span></span>

### <span data-ttu-id="a5e44-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a5e44-138">System.String</span></span>

### <span data-ttu-id="a5e44-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a5e44-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a5e44-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5e44-140">OUTPUTS</span></span>

### <span data-ttu-id="a5e44-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="a5e44-141">System.Void</span></span>

### <span data-ttu-id="a5e44-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e44-142">System.Boolean</span></span>

## <span data-ttu-id="a5e44-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5e44-143">NOTES</span></span>
<span data-ttu-id="a5e44-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="a5e44-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a5e44-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5e44-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5e44-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a5e44-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a5e44-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a5e44-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a5e44-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a5e44-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="a5e44-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="a5e44-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)