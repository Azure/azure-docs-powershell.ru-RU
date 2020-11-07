---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: fd87311c59c0889a57cb22eb08aba855e5c3b49c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729210"
---
# <span data-ttu-id="c704a-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c704a-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="c704a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c704a-102">SYNOPSIS</span></span>
<span data-ttu-id="c704a-103">Извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c704a-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c704a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c704a-104">SYNTAX</span></span>

### <span data-ttu-id="c704a-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c704a-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c704a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c704a-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c704a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c704a-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c704a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c704a-108">DESCRIPTION</span></span>
<span data-ttu-id="c704a-109">Параметр **Get-AzServiceBusGeoDRConfiguration** извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c704a-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="c704a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c704a-110">EXAMPLES</span></span>

### <span data-ttu-id="c704a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c704a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="c704a-112">Извлекает псевдоним "SampleDRCongifName" для основного пространства имен "SampleNamespace_Primary".</span><span class="sxs-lookup"><span data-stu-id="c704a-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="c704a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c704a-113">PARAMETERS</span></span>

### <span data-ttu-id="c704a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c704a-114">-DefaultProfile</span></span>
<span data-ttu-id="c704a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c704a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c704a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c704a-116">-InputObject</span></span>
<span data-ttu-id="c704a-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="c704a-117">Namespace Object</span></span>

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

### <span data-ttu-id="c704a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c704a-118">-Name</span></span>
<span data-ttu-id="c704a-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="c704a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c704a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c704a-120">-Namespace</span></span>
<span data-ttu-id="c704a-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c704a-121">Namespace Name</span></span>

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

### <span data-ttu-id="c704a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c704a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c704a-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c704a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c704a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c704a-124">-ResourceId</span></span>
<span data-ttu-id="c704a-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="c704a-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c704a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c704a-126">CommonParameters</span></span>
<span data-ttu-id="c704a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c704a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c704a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c704a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c704a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c704a-129">INPUTS</span></span>

### <span data-ttu-id="c704a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c704a-130">System.String</span></span>

### <span data-ttu-id="c704a-131">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c704a-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c704a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c704a-132">OUTPUTS</span></span>

### <span data-ttu-id="c704a-133">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c704a-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c704a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c704a-134">NOTES</span></span>

## <span data-ttu-id="c704a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c704a-135">RELATED LINKS</span></span>
