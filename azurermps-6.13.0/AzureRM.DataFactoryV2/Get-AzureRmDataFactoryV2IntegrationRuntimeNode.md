---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: e8f631b485c62dba2e3871d5c2deec69881097af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732971"
---
# <span data-ttu-id="1b1d0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1b1d0-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="1b1d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1d0-103">Получает сведения о узле среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-103">Gets an integration runtime node infomation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b1d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b1d0-104">SYNTAX</span></span>

### <span data-ttu-id="1b1d0-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b1d0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b1d0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1d0-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b1d0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1b1d0-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b1d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b1d0-108">DESCRIPTION</span></span>
<span data-ttu-id="1b1d0-109">Командлет **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** получает подробные сведения об узле среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-109">The **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="1b1d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b1d0-110">EXAMPLES</span></span>

### <span data-ttu-id="1b1d0-111">Пример 1: получение подробных сведений об узле среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

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

<span data-ttu-id="1b1d0-112">Командлет получает сведения о узле с именем "Node_1" в саморазмещенной среде выполнения Integration теста "Test-SelfHost-IR" в фабрике данных "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="1b1d0-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="1b1d0-113">Пример 2: получение подробных сведений об узле среды выполнения интеграции вместе с IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

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

<span data-ttu-id="1b1d0-114">Командлет получает сведения о узле с именем "Node_1" в саморазмещенной среде выполнения Test-SelfHost-IR в фабрике данных "Test-DF-Eu2", включая IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="1b1d0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b1d0-115">PARAMETERS</span></span>

### <span data-ttu-id="1b1d0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1b1d0-116">-DataFactoryName</span></span>
<span data-ttu-id="1b1d0-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-117">The data factory name.</span></span>

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

### <span data-ttu-id="1b1d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1d0-118">-DefaultProfile</span></span>
<span data-ttu-id="1b1d0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1d0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b1d0-120">-InputObject</span></span>
<span data-ttu-id="1b1d0-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="1b1d0-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1b1d0-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="1b1d0-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="1b1d0-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="1b1d0-124">-IpAddress</span></span>
<span data-ttu-id="1b1d0-125">IP-адрес узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="1b1d0-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b1d0-126">-Name</span></span>
<span data-ttu-id="1b1d0-127">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="1b1d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="1b1d0-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-129">The resource group name.</span></span>

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

### <span data-ttu-id="1b1d0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b1d0-130">-ResourceId</span></span>
<span data-ttu-id="1b1d0-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1b1d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1d0-132">CommonParameters</span></span>
<span data-ttu-id="1b1d0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b1d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1d0-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1d0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b1d0-135">INPUTS</span></span>

### <span data-ttu-id="1b1d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1b1d0-136">System.String</span></span>

### <span data-ttu-id="1b1d0-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1b1d0-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="1b1d0-138">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b1d0-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1b1d0-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b1d0-139">OUTPUTS</span></span>

### <span data-ttu-id="1b1d0-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1b1d0-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="1b1d0-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1b1d0-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="1b1d0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b1d0-142">NOTES</span></span>
<span data-ttu-id="1b1d0-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="1b1d0-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1b1d0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b1d0-144">RELATED LINKS</span></span>

[<span data-ttu-id="1b1d0-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1b1d0-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
