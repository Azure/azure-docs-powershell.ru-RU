---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236803"
---
# <span data-ttu-id="0697e-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0697e-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="0697e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0697e-102">SYNOPSIS</span></span>
<span data-ttu-id="0697e-103">Получает сведения о узле среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="0697e-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="0697e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0697e-104">SYNTAX</span></span>

### <span data-ttu-id="0697e-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0697e-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0697e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0697e-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0697e-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0697e-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0697e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0697e-108">DESCRIPTION</span></span>
<span data-ttu-id="0697e-109">Командлет **Get-AzDataFactoryV2IntegrationRuntimeNode** получает подробные сведения об узле среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="0697e-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="0697e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0697e-110">EXAMPLES</span></span>

### <span data-ttu-id="0697e-111">Пример 1: получение подробных сведений об узле среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0697e-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="0697e-112">Командлет получает сведения о узле с именем "Node_1" в саморазмещенной среде выполнения Integration теста "Test-SelfHost-IR" в фабрике данных "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="0697e-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="0697e-113">Пример 2: получение подробных сведений об узле среды выполнения интеграции вместе с IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="0697e-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="0697e-114">Командлет получает сведения о узле с именем "Node_1" в саморазмещенной среде выполнения Test-SelfHost-IR в фабрике данных "Test-DF-Eu2", включая IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0697e-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="0697e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0697e-115">PARAMETERS</span></span>

### <span data-ttu-id="0697e-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0697e-116">-DataFactoryName</span></span>
<span data-ttu-id="0697e-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0697e-117">The data factory name.</span></span>

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

### <span data-ttu-id="0697e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0697e-118">-DefaultProfile</span></span>
<span data-ttu-id="0697e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0697e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0697e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0697e-120">-InputObject</span></span>
<span data-ttu-id="0697e-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="0697e-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="0697e-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0697e-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0697e-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0697e-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="0697e-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="0697e-124">-IpAddress</span></span>
<span data-ttu-id="0697e-125">IP-адрес узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0697e-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="0697e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0697e-126">-Name</span></span>
<span data-ttu-id="0697e-127">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0697e-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="0697e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0697e-128">-ResourceGroupName</span></span>
<span data-ttu-id="0697e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0697e-129">The resource group name.</span></span>

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

### <span data-ttu-id="0697e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0697e-130">-ResourceId</span></span>
<span data-ttu-id="0697e-131">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0697e-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0697e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0697e-132">CommonParameters</span></span>
<span data-ttu-id="0697e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0697e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0697e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0697e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0697e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0697e-135">INPUTS</span></span>

### <span data-ttu-id="0697e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0697e-136">System.String</span></span>

### <span data-ttu-id="0697e-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0697e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0697e-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0697e-138">OUTPUTS</span></span>

### <span data-ttu-id="0697e-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0697e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="0697e-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0697e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="0697e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0697e-141">NOTES</span></span>
<span data-ttu-id="0697e-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="0697e-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0697e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0697e-143">RELATED LINKS</span></span>

[<span data-ttu-id="0697e-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0697e-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
