---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517481"
---
# <span data-ttu-id="5b221-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5b221-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="5b221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b221-102">SYNOPSIS</span></span>
<span data-ttu-id="5b221-103">Извлекает migrationConfiguration для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5b221-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="5b221-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b221-104">SYNTAX</span></span>

### <span data-ttu-id="5b221-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b221-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b221-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b221-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b221-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b221-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b221-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b221-108">DESCRIPTION</span></span>
<span data-ttu-id="5b221-109">**Get-AzServiceBusMigration** извлекает конфигурацию миграции для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5b221-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="5b221-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b221-110">EXAMPLES</span></span>

### <span data-ttu-id="5b221-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b221-111">Example 1</span></span>
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

<span data-ttu-id="5b221-112">Свойства конфигурации миграции testingNamespaceStandardMigration</span><span class="sxs-lookup"><span data-stu-id="5b221-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="5b221-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b221-113">PARAMETERS</span></span>

### <span data-ttu-id="5b221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b221-114">-DefaultProfile</span></span>
<span data-ttu-id="5b221-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b221-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b221-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b221-116">-InputObject</span></span>
<span data-ttu-id="5b221-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="5b221-117">Namespace Object</span></span>

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

### <span data-ttu-id="5b221-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5b221-118">-Name</span></span>
<span data-ttu-id="5b221-119">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5b221-119">Namespace Name</span></span>

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

### <span data-ttu-id="5b221-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b221-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b221-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5b221-121">Resource Group Name</span></span>

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

### <span data-ttu-id="5b221-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b221-122">-ResourceId</span></span>
<span data-ttu-id="5b221-123">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="5b221-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="5b221-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b221-124">CommonParameters</span></span>
<span data-ttu-id="5b221-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b221-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b221-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b221-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b221-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b221-127">INPUTS</span></span>

### <span data-ttu-id="5b221-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5b221-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="5b221-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5b221-129">System.String</span></span>

## <span data-ttu-id="5b221-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b221-130">OUTPUTS</span></span>

### <span data-ttu-id="5b221-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5b221-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="5b221-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b221-132">NOTES</span></span>

## <span data-ttu-id="5b221-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b221-133">RELATED LINKS</span></span>
