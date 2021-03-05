---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a3b3c25ce424085597de7396be469356f3d3f1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975171"
---
# <span data-ttu-id="95f70-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="95f70-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="95f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f70-102">SYNOPSIS</span></span>
<span data-ttu-id="95f70-103">Возвращает сведения об узле узла для интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="95f70-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="95f70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95f70-104">SYNTAX</span></span>

### <span data-ttu-id="95f70-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95f70-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95f70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="95f70-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f70-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="95f70-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f70-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f70-108">DESCRIPTION</span></span>
<span data-ttu-id="95f70-109">**Cmdlet Get-AzDataFactoryV2IntegrationRuntimeNode** получает подробные сведения об узле времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="95f70-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="95f70-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95f70-110">EXAMPLES</span></span>

### <span data-ttu-id="95f70-111">Пример 1. Возвращает подробные сведения об узле времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="95f70-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="95f70-112">Он получает сведения о узле Node_1 в режиме самостоятельной интеграции "test-selfhost-ir" в фабрике данных test-df-eu2.</span><span class="sxs-lookup"><span data-stu-id="95f70-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="95f70-113">Пример 2. Получает подробные сведения об узле интеграции runtime вместе с IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="95f70-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="95f70-114">Он получает сведения узла Node_1 в режиме самостоятельной интеграции "test-selfhost-ir" в фабрике данных test-df-eu2, включая IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="95f70-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="95f70-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95f70-115">PARAMETERS</span></span>

### <span data-ttu-id="95f70-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="95f70-116">-DataFactoryName</span></span>
<span data-ttu-id="95f70-117">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="95f70-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f70-118">-DefaultProfile</span></span>
<span data-ttu-id="95f70-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95f70-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f70-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95f70-120">-InputObject</span></span>
<span data-ttu-id="95f70-121">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="95f70-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95f70-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="95f70-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="95f70-123">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="95f70-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f70-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="95f70-124">-IpAddress</span></span>
<span data-ttu-id="95f70-125">IP-адрес узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="95f70-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="95f70-126">-Name</span><span class="sxs-lookup"><span data-stu-id="95f70-126">-Name</span></span>
<span data-ttu-id="95f70-127">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="95f70-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f70-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f70-128">-ResourceGroupName</span></span>
<span data-ttu-id="95f70-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95f70-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f70-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95f70-130">-ResourceId</span></span>
<span data-ttu-id="95f70-131">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="95f70-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f70-132">CommonParameters</span></span>
<span data-ttu-id="95f70-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f70-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f70-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f70-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95f70-135">INPUTS</span></span>

### <span data-ttu-id="95f70-136">System.String</span><span class="sxs-lookup"><span data-stu-id="95f70-136">System.String</span></span>

### <span data-ttu-id="95f70-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="95f70-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="95f70-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95f70-138">OUTPUTS</span></span>

### <span data-ttu-id="95f70-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="95f70-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="95f70-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="95f70-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="95f70-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95f70-141">NOTES</span></span>
<span data-ttu-id="95f70-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="95f70-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="95f70-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95f70-143">RELATED LINKS</span></span>

[<span data-ttu-id="95f70-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="95f70-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
