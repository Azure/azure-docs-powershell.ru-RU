---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407431"
---
# <span data-ttu-id="625bc-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="625bc-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="625bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625bc-102">SYNOPSIS</span></span>
<span data-ttu-id="625bc-103">Все активные сеансы отлагки потоков данных отлагожки в фабрике данных Azure</span><span class="sxs-lookup"><span data-stu-id="625bc-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="625bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="625bc-104">SYNTAX</span></span>

### <span data-ttu-id="625bc-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="625bc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="625bc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="625bc-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="625bc-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="625bc-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="625bc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="625bc-108">DESCRIPTION</span></span>
<span data-ttu-id="625bc-109">Со списком всех сеансов отламывки потоков данных, которые работает фабрика данных Azure, с подробными сведениями.</span><span class="sxs-lookup"><span data-stu-id="625bc-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="625bc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="625bc-110">EXAMPLES</span></span>

### <span data-ttu-id="625bc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="625bc-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="625bc-112">Получите все активные сеансы отладки потоков данных на фабрике данных Azure "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="625bc-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="625bc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="625bc-113">PARAMETERS</span></span>

### <span data-ttu-id="625bc-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="625bc-114">-DataFactory</span></span>
<span data-ttu-id="625bc-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="625bc-115">The data factory object.</span></span>

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

### <span data-ttu-id="625bc-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="625bc-116">-DataFactoryName</span></span>
<span data-ttu-id="625bc-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="625bc-117">The data factory name.</span></span>

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

### <span data-ttu-id="625bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625bc-118">-DefaultProfile</span></span>
<span data-ttu-id="625bc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="625bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="625bc-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="625bc-121">The resource group name.</span></span>

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

### <span data-ttu-id="625bc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="625bc-122">-ResourceId</span></span>
<span data-ttu-id="625bc-123">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="625bc-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="625bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625bc-124">CommonParameters</span></span>
<span data-ttu-id="625bc-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625bc-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="625bc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625bc-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="625bc-127">INPUTS</span></span>

### <span data-ttu-id="625bc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="625bc-128">System.String</span></span>

### <span data-ttu-id="625bc-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="625bc-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="625bc-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="625bc-130">OUTPUTS</span></span>

### <span data-ttu-id="625bc-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="625bc-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="625bc-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="625bc-132">NOTES</span></span>
<span data-ttu-id="625bc-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="625bc-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="625bc-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="625bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="625bc-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="625bc-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="625bc-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="625bc-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="625bc-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="625bc-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="625bc-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="625bc-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)