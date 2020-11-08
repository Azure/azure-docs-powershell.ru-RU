---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073751"
---
# <span data-ttu-id="f05e0-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f05e0-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="f05e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f05e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f05e0-103">Извлекает MigrationConfiguration для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f05e0-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="f05e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f05e0-104">SYNTAX</span></span>

### <span data-ttu-id="f05e0-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f05e0-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f05e0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f05e0-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f05e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05e0-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f05e0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f05e0-108">DESCRIPTION</span></span>
<span data-ttu-id="f05e0-109">Элемент **Get-AzServiceBusMigration** получает конфигурацию миграции для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f05e0-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="f05e0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f05e0-110">EXAMPLES</span></span>

### <span data-ttu-id="f05e0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f05e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="f05e0-112">Возвращает свойства конфигурации миграции "TestingNamespaceStandardMigration".</span><span class="sxs-lookup"><span data-stu-id="f05e0-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="f05e0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f05e0-113">PARAMETERS</span></span>

### <span data-ttu-id="f05e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05e0-114">-DefaultProfile</span></span>
<span data-ttu-id="f05e0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f05e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05e0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f05e0-116">-InputObject</span></span>
<span data-ttu-id="f05e0-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="f05e0-117">Namespace Object</span></span>

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

### <span data-ttu-id="f05e0-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f05e0-118">-Name</span></span>
<span data-ttu-id="f05e0-119">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f05e0-119">Namespace Name</span></span>

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

### <span data-ttu-id="f05e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="f05e0-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f05e0-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f05e0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f05e0-122">-ResourceId</span></span>
<span data-ttu-id="f05e0-123">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="f05e0-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f05e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05e0-124">CommonParameters</span></span>
<span data-ttu-id="f05e0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f05e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05e0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05e0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f05e0-127">INPUTS</span></span>

### <span data-ttu-id="f05e0-128">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f05e0-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="f05e0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f05e0-129">System.String</span></span>

## <span data-ttu-id="f05e0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f05e0-130">OUTPUTS</span></span>

### <span data-ttu-id="f05e0-131">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f05e0-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="f05e0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f05e0-132">NOTES</span></span>

## <span data-ttu-id="f05e0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f05e0-133">RELATED LINKS</span></span>
