---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565363"
---
# <span data-ttu-id="79cf2-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="79cf2-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="79cf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="79cf2-103">Создание новой конфигурации миграции и начало миграции сущностей из стандартного в расширенное пространство имен</span><span class="sxs-lookup"><span data-stu-id="79cf2-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79cf2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79cf2-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79cf2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="79cf2-106">Командлет **Start-AzureRmServiceBusMigration** создает новую конфигурацию миграции и начинает миграцию сущностей из стандартных в расширенные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="79cf2-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="79cf2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79cf2-107">EXAMPLES</span></span>

### <span data-ttu-id="79cf2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79cf2-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="79cf2-109">Создает новую конфигурацию миграции для пространств имен "TestingNamespaceStandardMirgation" и "TestingNamespacePremiumMirgation"</span><span class="sxs-lookup"><span data-stu-id="79cf2-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="79cf2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79cf2-110">PARAMETERS</span></span>

### <span data-ttu-id="79cf2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79cf2-111">-AsJob</span></span>
<span data-ttu-id="79cf2-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="79cf2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79cf2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79cf2-113">-DefaultProfile</span></span>
<span data-ttu-id="79cf2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79cf2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79cf2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79cf2-115">-Name</span></span>
<span data-ttu-id="79cf2-116">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="79cf2-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79cf2-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="79cf2-117">-PostMigrationName</span></span>
<span data-ttu-id="79cf2-118">Имя после миграции для пространства имен standrad в миграции</span><span class="sxs-lookup"><span data-stu-id="79cf2-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79cf2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79cf2-119">-ResourceGroupName</span></span>
<span data-ttu-id="79cf2-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="79cf2-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79cf2-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="79cf2-121">-TargetNameSpace</span></span>
<span data-ttu-id="79cf2-122">Идентификатор ARM для пространства имен Premium</span><span class="sxs-lookup"><span data-stu-id="79cf2-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79cf2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79cf2-123">-Confirm</span></span>
<span data-ttu-id="79cf2-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79cf2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79cf2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79cf2-125">-WhatIf</span></span>
<span data-ttu-id="79cf2-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79cf2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79cf2-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79cf2-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79cf2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79cf2-128">CommonParameters</span></span>
<span data-ttu-id="79cf2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79cf2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79cf2-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79cf2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79cf2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79cf2-131">INPUTS</span></span>

### <span data-ttu-id="79cf2-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="79cf2-132">None</span></span>

## <span data-ttu-id="79cf2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79cf2-133">OUTPUTS</span></span>

### <span data-ttu-id="79cf2-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="79cf2-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="79cf2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="79cf2-135">NOTES</span></span>

## <span data-ttu-id="79cf2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79cf2-136">RELATED LINKS</span></span>
