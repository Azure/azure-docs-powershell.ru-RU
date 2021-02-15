---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242248"
---
# <span data-ttu-id="a446f-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a446f-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="a446f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a446f-102">SYNOPSIS</span></span>
<span data-ttu-id="a446f-103">Извлекает псевдоним (конфигурация аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a446f-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="a446f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a446f-104">SYNTAX</span></span>

### <span data-ttu-id="a446f-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a446f-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a446f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a446f-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a446f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a446f-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a446f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a446f-108">DESCRIPTION</span></span>
<span data-ttu-id="a446f-109">The **Get-AzServiceBusGeoDRConfiguration** retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span><span class="sxs-lookup"><span data-stu-id="a446f-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="a446f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a446f-110">EXAMPLES</span></span>

### <span data-ttu-id="a446f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a446f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="a446f-112">Извлекает псевдоним SampleDRConfigName для основного пространства имен "SampleNamespace_Primary".</span><span class="sxs-lookup"><span data-stu-id="a446f-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="a446f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a446f-113">PARAMETERS</span></span>

### <span data-ttu-id="a446f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a446f-114">-DefaultProfile</span></span>
<span data-ttu-id="a446f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a446f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a446f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a446f-116">-InputObject</span></span>
<span data-ttu-id="a446f-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="a446f-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a446f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a446f-118">-Name</span></span>
<span data-ttu-id="a446f-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="a446f-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a446f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a446f-120">-Namespace</span></span>
<span data-ttu-id="a446f-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a446f-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a446f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a446f-122">-ResourceGroupName</span></span>
<span data-ttu-id="a446f-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a446f-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a446f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a446f-124">-ResourceId</span></span>
<span data-ttu-id="a446f-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="a446f-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a446f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a446f-126">CommonParameters</span></span>
<span data-ttu-id="a446f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a446f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a446f-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a446f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a446f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a446f-129">INPUTS</span></span>

### <span data-ttu-id="a446f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a446f-130">System.String</span></span>

### <span data-ttu-id="a446f-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a446f-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a446f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a446f-132">OUTPUTS</span></span>

### <span data-ttu-id="a446f-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a446f-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="a446f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a446f-134">NOTES</span></span>

## <span data-ttu-id="a446f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a446f-135">RELATED LINKS</span></span>
