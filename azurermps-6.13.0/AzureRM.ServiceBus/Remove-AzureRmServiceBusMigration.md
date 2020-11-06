---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562619"
---
# <span data-ttu-id="1e720-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1e720-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="1e720-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e720-102">SYNOPSIS</span></span>
<span data-ttu-id="1e720-103">Командлет удаляет конфигурацию миграции для стандартных и расширенных пространств имен.</span><span class="sxs-lookup"><span data-stu-id="1e720-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e720-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e720-104">SYNTAX</span></span>

### <span data-ttu-id="1e720-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e720-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e720-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e720-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e720-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e720-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e720-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e720-108">DESCRIPTION</span></span>
<span data-ttu-id="1e720-109">Командлет **Remove-AzureRmServiceBusMigration** удаляет конфигурацию миграции для Standard to Premium Namespaces</span><span class="sxs-lookup"><span data-stu-id="1e720-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="1e720-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e720-110">EXAMPLES</span></span>

### <span data-ttu-id="1e720-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e720-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="1e720-112">Удаление конфигурации миграции "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="1e720-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="1e720-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e720-113">PARAMETERS</span></span>

### <span data-ttu-id="1e720-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e720-114">-AsJob</span></span>
<span data-ttu-id="1e720-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1e720-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e720-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e720-116">-DefaultProfile</span></span>
<span data-ttu-id="1e720-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e720-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e720-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e720-118">-InputObject</span></span>
<span data-ttu-id="1e720-119">Объект стандартного пространства имен для миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="1e720-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e720-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e720-120">-Name</span></span>
<span data-ttu-id="1e720-121">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="1e720-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="1e720-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e720-122">-PassThru</span></span>
<span data-ttu-id="1e720-123">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1e720-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1e720-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e720-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e720-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e720-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1e720-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e720-126">-ResourceId</span></span>
<span data-ttu-id="1e720-127">Идентификатор ресурса стандартного пространства имен для миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="1e720-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e720-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e720-128">-Confirm</span></span>
<span data-ttu-id="1e720-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e720-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e720-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e720-130">-WhatIf</span></span>
<span data-ttu-id="1e720-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e720-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e720-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e720-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e720-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e720-133">CommonParameters</span></span>
<span data-ttu-id="1e720-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e720-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e720-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e720-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e720-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e720-136">INPUTS</span></span>

### <span data-ttu-id="1e720-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1e720-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="1e720-138">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1e720-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1e720-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1e720-139">System.String</span></span>

## <span data-ttu-id="1e720-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e720-140">OUTPUTS</span></span>

### <span data-ttu-id="1e720-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e720-141">System.Boolean</span></span>

## <span data-ttu-id="1e720-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e720-142">NOTES</span></span>

## <span data-ttu-id="1e720-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e720-143">RELATED LINKS</span></span>
