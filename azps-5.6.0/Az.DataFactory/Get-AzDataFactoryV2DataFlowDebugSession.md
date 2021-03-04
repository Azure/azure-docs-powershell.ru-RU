---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 35acbbaeb4983def89711049fc3284a63611bbec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975283"
---
# <span data-ttu-id="87b51-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="87b51-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="87b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b51-102">SYNOPSIS</span></span>
<span data-ttu-id="87b51-103">Получите все активные сеансы отламки потоков данных отлагововодной фабрики данных Azure</span><span class="sxs-lookup"><span data-stu-id="87b51-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="87b51-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87b51-104">SYNTAX</span></span>

### <span data-ttu-id="87b51-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87b51-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b51-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87b51-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87b51-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="87b51-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b51-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87b51-108">DESCRIPTION</span></span>
<span data-ttu-id="87b51-109">Со списком всех сеансов отламывки потоков активных данных, которые работает фабрика данных Azure, с подробными сведениями.</span><span class="sxs-lookup"><span data-stu-id="87b51-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="87b51-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87b51-110">EXAMPLES</span></span>

### <span data-ttu-id="87b51-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87b51-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="87b51-112">Получите все активные сеансы отладки потоков данных на фабрике данных Azure "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="87b51-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="87b51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87b51-113">PARAMETERS</span></span>

### <span data-ttu-id="87b51-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="87b51-114">-DataFactory</span></span>
<span data-ttu-id="87b51-115">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="87b51-115">The data factory object.</span></span>

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

### <span data-ttu-id="87b51-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="87b51-116">-DataFactoryName</span></span>
<span data-ttu-id="87b51-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="87b51-117">The data factory name.</span></span>

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

### <span data-ttu-id="87b51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b51-118">-DefaultProfile</span></span>
<span data-ttu-id="87b51-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87b51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87b51-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b51-120">-ResourceGroupName</span></span>
<span data-ttu-id="87b51-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87b51-121">The resource group name.</span></span>

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

### <span data-ttu-id="87b51-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b51-122">-ResourceId</span></span>
<span data-ttu-id="87b51-123">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="87b51-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="87b51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b51-124">CommonParameters</span></span>
<span data-ttu-id="87b51-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b51-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87b51-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b51-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87b51-127">INPUTS</span></span>

### <span data-ttu-id="87b51-128">System.String</span><span class="sxs-lookup"><span data-stu-id="87b51-128">System.String</span></span>

### <span data-ttu-id="87b51-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="87b51-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="87b51-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87b51-130">OUTPUTS</span></span>

### <span data-ttu-id="87b51-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="87b51-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="87b51-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87b51-132">NOTES</span></span>
<span data-ttu-id="87b51-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="87b51-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="87b51-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87b51-134">RELATED LINKS</span></span>

[<span data-ttu-id="87b51-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="87b51-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="87b51-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="87b51-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="87b51-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="87b51-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="87b51-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="87b51-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)