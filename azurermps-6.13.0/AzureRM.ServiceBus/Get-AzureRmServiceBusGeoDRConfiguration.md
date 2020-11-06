---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 7d3635b33e96052c42ca77384d2f138af5cc0d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567237"
---
# <span data-ttu-id="2e705-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e705-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2e705-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e705-102">SYNOPSIS</span></span>
<span data-ttu-id="2e705-103">Извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2e705-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e705-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e705-104">SYNTAX</span></span>

### <span data-ttu-id="2e705-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e705-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e705-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e705-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e705-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e705-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e705-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e705-108">DESCRIPTION</span></span>
<span data-ttu-id="2e705-109">Параметр **Get-AzureRmServiceBusGeoDRConfiguration** извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2e705-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="2e705-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e705-110">EXAMPLES</span></span>

### <span data-ttu-id="2e705-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e705-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="2e705-112">Извлекает псевдоним "SampleDRCongifName" для основного пространства имен "SampleNamespace_Primary".</span><span class="sxs-lookup"><span data-stu-id="2e705-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="2e705-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e705-113">PARAMETERS</span></span>

### <span data-ttu-id="2e705-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e705-114">-DefaultProfile</span></span>
<span data-ttu-id="2e705-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e705-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e705-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e705-116">-InputObject</span></span>
<span data-ttu-id="2e705-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="2e705-117">Namespace Object</span></span>

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

### <span data-ttu-id="2e705-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e705-118">-Name</span></span>
<span data-ttu-id="2e705-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="2e705-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="2e705-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e705-120">-Namespace</span></span>
<span data-ttu-id="2e705-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2e705-121">Namespace Name</span></span>

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

### <span data-ttu-id="2e705-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e705-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e705-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2e705-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2e705-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e705-124">-ResourceId</span></span>
<span data-ttu-id="2e705-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="2e705-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2e705-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e705-126">CommonParameters</span></span>
<span data-ttu-id="2e705-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e705-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e705-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e705-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e705-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e705-129">INPUTS</span></span>

### <span data-ttu-id="2e705-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2e705-130">System.String</span></span>

### <span data-ttu-id="2e705-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2e705-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="2e705-132">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e705-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2e705-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e705-133">OUTPUTS</span></span>

### <span data-ttu-id="2e705-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2e705-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2e705-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e705-135">NOTES</span></span>

## <span data-ttu-id="2e705-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e705-136">RELATED LINKS</span></span>
