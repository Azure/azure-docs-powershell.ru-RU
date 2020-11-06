---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565371"
---
# <span data-ttu-id="240e0-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="240e0-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="240e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="240e0-102">SYNOPSIS</span></span>
<span data-ttu-id="240e0-103">Извлекает MigrationConfiguration для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="240e0-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="240e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="240e0-104">SYNTAX</span></span>

### <span data-ttu-id="240e0-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="240e0-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="240e0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="240e0-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="240e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="240e0-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="240e0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="240e0-108">DESCRIPTION</span></span>
<span data-ttu-id="240e0-109">Элемент **Get-AzureRmServiceBusMigration** получает конфигурацию миграции для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="240e0-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="240e0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="240e0-110">EXAMPLES</span></span>

### <span data-ttu-id="240e0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="240e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="240e0-112">Возвращает свойства конфигурации миграции "TestingNamespaceStandardMirgation".</span><span class="sxs-lookup"><span data-stu-id="240e0-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="240e0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="240e0-113">PARAMETERS</span></span>

### <span data-ttu-id="240e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240e0-114">-DefaultProfile</span></span>
<span data-ttu-id="240e0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="240e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240e0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="240e0-116">-InputObject</span></span>
<span data-ttu-id="240e0-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="240e0-117">Namespace Object</span></span>

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

### <span data-ttu-id="240e0-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="240e0-118">-Name</span></span>
<span data-ttu-id="240e0-119">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="240e0-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="240e0-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="240e0-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240e0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="240e0-122">-ResourceId</span></span>
<span data-ttu-id="240e0-123">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="240e0-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="240e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240e0-124">CommonParameters</span></span>
<span data-ttu-id="240e0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="240e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240e0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="240e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240e0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="240e0-127">INPUTS</span></span>

### <span data-ttu-id="240e0-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="240e0-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="240e0-129">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="240e0-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="240e0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="240e0-130">System.String</span></span>

## <span data-ttu-id="240e0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="240e0-131">OUTPUTS</span></span>

### <span data-ttu-id="240e0-132">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="240e0-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="240e0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="240e0-133">NOTES</span></span>

## <span data-ttu-id="240e0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="240e0-134">RELATED LINKS</span></span>
