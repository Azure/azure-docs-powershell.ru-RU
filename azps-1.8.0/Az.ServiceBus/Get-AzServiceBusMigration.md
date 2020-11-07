---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: b78836a7d122dc05e4cd621b2d8994bd55697687
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729205"
---
# <span data-ttu-id="134ad-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="134ad-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="134ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="134ad-102">SYNOPSIS</span></span>
<span data-ttu-id="134ad-103">Извлекает MigrationConfiguration для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="134ad-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="134ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="134ad-104">SYNTAX</span></span>

### <span data-ttu-id="134ad-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="134ad-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="134ad-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="134ad-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="134ad-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="134ad-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="134ad-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="134ad-108">DESCRIPTION</span></span>
<span data-ttu-id="134ad-109">Элемент **Get-AzServiceBusMigration** получает конфигурацию миграции для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="134ad-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="134ad-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="134ad-110">EXAMPLES</span></span>

### <span data-ttu-id="134ad-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="134ad-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="134ad-112">Возвращает свойства конфигурации миграции "TestingNamespaceStandardMirgation".</span><span class="sxs-lookup"><span data-stu-id="134ad-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="134ad-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="134ad-113">PARAMETERS</span></span>

### <span data-ttu-id="134ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134ad-114">-DefaultProfile</span></span>
<span data-ttu-id="134ad-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="134ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="134ad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="134ad-116">-InputObject</span></span>
<span data-ttu-id="134ad-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="134ad-117">Namespace Object</span></span>

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

### <span data-ttu-id="134ad-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="134ad-118">-Name</span></span>
<span data-ttu-id="134ad-119">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="134ad-119">Namespace Name</span></span>

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

### <span data-ttu-id="134ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="134ad-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="134ad-121">Resource Group Name</span></span>

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

### <span data-ttu-id="134ad-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="134ad-122">-ResourceId</span></span>
<span data-ttu-id="134ad-123">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="134ad-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="134ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134ad-124">CommonParameters</span></span>
<span data-ttu-id="134ad-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="134ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134ad-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="134ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134ad-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="134ad-127">INPUTS</span></span>

### <span data-ttu-id="134ad-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="134ad-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="134ad-129">System. String</span><span class="sxs-lookup"><span data-stu-id="134ad-129">System.String</span></span>

## <span data-ttu-id="134ad-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="134ad-130">OUTPUTS</span></span>

### <span data-ttu-id="134ad-131">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="134ad-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="134ad-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="134ad-132">NOTES</span></span>

## <span data-ttu-id="134ad-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="134ad-133">RELATED LINKS</span></span>
