---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 9d8afa31d296e62c75b869bd93e6f96aadf82328
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731361"
---
# <span data-ttu-id="0d397-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0d397-101">Get-AzContainerService</span></span>

## <span data-ttu-id="0d397-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d397-102">SYNOPSIS</span></span>
<span data-ttu-id="0d397-103">Возвращает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="0d397-103">Gets a container service.</span></span>

## <span data-ttu-id="0d397-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d397-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d397-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d397-105">DESCRIPTION</span></span>
<span data-ttu-id="0d397-106">Командлет **Get-AzContainerService** Получает службу контейнеров.</span><span class="sxs-lookup"><span data-stu-id="0d397-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="0d397-107">Вы можете просматривать свойства службы контейнеров, в том числе состояние, количество основных и агентов, а также полное доменное имя главного и агента.</span><span class="sxs-lookup"><span data-stu-id="0d397-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="0d397-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d397-108">EXAMPLES</span></span>

### <span data-ttu-id="0d397-109">Пример 1: получение службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="0d397-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="0d397-110">Эта команда получает службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0d397-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="0d397-111">Пример 2: получение всех служб контейнеров</span><span class="sxs-lookup"><span data-stu-id="0d397-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="0d397-112">Эта команда получает все службы контейнеров в подписке.</span><span class="sxs-lookup"><span data-stu-id="0d397-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="0d397-113">Пример 3: получение всех служб контейнеров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="0d397-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="0d397-114">Эта команда получает все службы контейнеров в ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0d397-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="0d397-115">Пример 4: получение всех служб контейнеров с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="0d397-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="0d397-116">Эта команда получает все службы контейнеров, начинающиеся с "CSResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="0d397-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="0d397-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d397-117">PARAMETERS</span></span>

### <span data-ttu-id="0d397-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d397-118">-DefaultProfile</span></span>
<span data-ttu-id="0d397-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d397-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d397-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d397-120">-Name</span></span>
<span data-ttu-id="0d397-121">Указывает имя службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d397-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0d397-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d397-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d397-123">Указывает группу ресурсов для службы контейнеров, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d397-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0d397-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d397-124">CommonParameters</span></span>
<span data-ttu-id="0d397-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d397-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d397-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d397-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d397-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d397-127">INPUTS</span></span>

### <span data-ttu-id="0d397-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d397-128">System.String</span></span>

## <span data-ttu-id="0d397-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d397-129">OUTPUTS</span></span>

### <span data-ttu-id="0d397-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="0d397-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0d397-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d397-131">NOTES</span></span>

## <span data-ttu-id="0d397-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d397-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d397-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0d397-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="0d397-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0d397-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="0d397-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0d397-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


