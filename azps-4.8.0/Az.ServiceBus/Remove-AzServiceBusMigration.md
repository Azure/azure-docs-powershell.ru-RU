---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236623"
---
# <span data-ttu-id="304ca-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="304ca-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="304ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="304ca-102">SYNOPSIS</span></span>
<span data-ttu-id="304ca-103">Командлет удаляет конфигурацию миграции для стандартных и расширенных пространств имен.</span><span class="sxs-lookup"><span data-stu-id="304ca-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="304ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="304ca-104">SYNTAX</span></span>

### <span data-ttu-id="304ca-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="304ca-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304ca-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="304ca-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304ca-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="304ca-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="304ca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="304ca-108">DESCRIPTION</span></span>
<span data-ttu-id="304ca-109">Командлет **Remove-AzServiceBusMigration** удаляет конфигурацию миграции для Standard to Premium Namespaces</span><span class="sxs-lookup"><span data-stu-id="304ca-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="304ca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="304ca-110">EXAMPLES</span></span>

### <span data-ttu-id="304ca-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="304ca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="304ca-112">Удаление конфигурации миграции "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="304ca-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="304ca-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="304ca-113">PARAMETERS</span></span>

### <span data-ttu-id="304ca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="304ca-114">-AsJob</span></span>
<span data-ttu-id="304ca-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="304ca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="304ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304ca-116">-DefaultProfile</span></span>
<span data-ttu-id="304ca-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="304ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304ca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="304ca-118">-InputObject</span></span>
<span data-ttu-id="304ca-119">Объект стандартного пространства имен для миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="304ca-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="304ca-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="304ca-120">-Name</span></span>
<span data-ttu-id="304ca-121">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="304ca-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="304ca-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="304ca-122">-PassThru</span></span>
<span data-ttu-id="304ca-123">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="304ca-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="304ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="304ca-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="304ca-125">Resource Group Name</span></span>

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

### <span data-ttu-id="304ca-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="304ca-126">-ResourceId</span></span>
<span data-ttu-id="304ca-127">Идентификатор ресурса стандартного пространства имен для миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="304ca-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="304ca-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="304ca-128">-Confirm</span></span>
<span data-ttu-id="304ca-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="304ca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304ca-130">-WhatIf</span></span>
<span data-ttu-id="304ca-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="304ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="304ca-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="304ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304ca-133">CommonParameters</span></span>
<span data-ttu-id="304ca-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="304ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304ca-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="304ca-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304ca-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="304ca-136">INPUTS</span></span>

### <span data-ttu-id="304ca-137">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="304ca-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="304ca-138">System. String</span><span class="sxs-lookup"><span data-stu-id="304ca-138">System.String</span></span>

## <span data-ttu-id="304ca-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="304ca-139">OUTPUTS</span></span>

### <span data-ttu-id="304ca-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="304ca-140">System.Boolean</span></span>

## <span data-ttu-id="304ca-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="304ca-141">NOTES</span></span>

## <span data-ttu-id="304ca-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="304ca-142">RELATED LINKS</span></span>