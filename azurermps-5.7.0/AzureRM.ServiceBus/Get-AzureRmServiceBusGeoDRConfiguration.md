---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561484"
---
# <span data-ttu-id="d67b3-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d67b3-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="d67b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d67b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d67b3-103">Извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d67b3-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d67b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d67b3-104">SYNTAX</span></span>

### <span data-ttu-id="d67b3-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d67b3-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d67b3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d67b3-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d67b3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d67b3-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67b3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67b3-108">DESCRIPTION</span></span>
<span data-ttu-id="d67b3-109">Параметр **Get-AzureRmServiceBusGeoDRConfiguration** извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d67b3-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="d67b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d67b3-110">EXAMPLES</span></span>

### <span data-ttu-id="d67b3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d67b3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="d67b3-112">Извлекает псевдоним "SampleDRCongifName" для основного пространства имен "SampleNamespace_Primary".</span><span class="sxs-lookup"><span data-stu-id="d67b3-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="d67b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d67b3-113">PARAMETERS</span></span>

### <span data-ttu-id="d67b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67b3-114">-DefaultProfile</span></span>
<span data-ttu-id="d67b3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d67b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67b3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d67b3-116">-InputObject</span></span>
<span data-ttu-id="d67b3-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="d67b3-117">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d67b3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d67b3-118">-Name</span></span>
<span data-ttu-id="d67b3-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="d67b3-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67b3-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d67b3-120">-Namespace</span></span>
<span data-ttu-id="d67b3-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="d67b3-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="d67b3-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d67b3-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67b3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d67b3-124">-ResourceId</span></span>
<span data-ttu-id="d67b3-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="d67b3-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67b3-126">CommonParameters</span></span>
<span data-ttu-id="d67b3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d67b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d67b3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67b3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d67b3-129">INPUTS</span></span>

### <span data-ttu-id="d67b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d67b3-130">System.String</span></span>
<span data-ttu-id="d67b3-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d67b3-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="d67b3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67b3-132">OUTPUTS</span></span>

### <span data-ttu-id="d67b3-133">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="d67b3-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="d67b3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="d67b3-134">NOTES</span></span>

## <span data-ttu-id="d67b3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d67b3-135">RELATED LINKS</span></span>
