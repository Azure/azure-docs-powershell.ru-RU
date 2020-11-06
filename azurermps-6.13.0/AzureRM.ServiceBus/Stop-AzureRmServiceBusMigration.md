---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565356"
---
# <span data-ttu-id="32e08-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="32e08-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="32e08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32e08-102">SYNOPSIS</span></span>
<span data-ttu-id="32e08-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="32e08-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32e08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32e08-104">SYNTAX</span></span>

### <span data-ttu-id="32e08-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32e08-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32e08-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="32e08-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32e08-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32e08-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32e08-108">DESCRIPTION</span></span>
<span data-ttu-id="32e08-109">Командлеты **Stop-AzureRmServiceBusMigration** tremitates миграцию между стандартным пространством имен Standard и Premium</span><span class="sxs-lookup"><span data-stu-id="32e08-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="32e08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32e08-110">EXAMPLES</span></span>

### <span data-ttu-id="32e08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32e08-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="32e08-112">Командлет termitates миграцию между стандартным пространством имен и пространством имен Premium, указанное при создании конфигурации миграции.</span><span class="sxs-lookup"><span data-stu-id="32e08-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="32e08-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32e08-113">PARAMETERS</span></span>

### <span data-ttu-id="32e08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e08-114">-DefaultProfile</span></span>
<span data-ttu-id="32e08-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32e08-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32e08-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32e08-116">-InputObject</span></span>
<span data-ttu-id="32e08-117">Объект стандартного пространства имен для настройки миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="32e08-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="32e08-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32e08-118">-Name</span></span>
<span data-ttu-id="32e08-119">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="32e08-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="32e08-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32e08-120">-PassThru</span></span>
<span data-ttu-id="32e08-121">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="32e08-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="32e08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e08-122">-ResourceGroupName</span></span>
<span data-ttu-id="32e08-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="32e08-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e08-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32e08-124">-ResourceId</span></span>
<span data-ttu-id="32e08-125">Идентификатор ресурса стандартного пространства имен для настройки миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="32e08-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="32e08-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32e08-126">-Confirm</span></span>
<span data-ttu-id="32e08-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32e08-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e08-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e08-128">-WhatIf</span></span>
<span data-ttu-id="32e08-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32e08-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32e08-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32e08-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e08-131">CommonParameters</span></span>
<span data-ttu-id="32e08-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32e08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e08-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e08-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e08-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32e08-134">INPUTS</span></span>

### <span data-ttu-id="32e08-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="32e08-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="32e08-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32e08-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="32e08-137">System. String</span><span class="sxs-lookup"><span data-stu-id="32e08-137">System.String</span></span>

## <span data-ttu-id="32e08-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32e08-138">OUTPUTS</span></span>

### <span data-ttu-id="32e08-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32e08-139">System.Boolean</span></span>

## <span data-ttu-id="32e08-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="32e08-140">NOTES</span></span>

## <span data-ttu-id="32e08-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32e08-141">RELATED LINKS</span></span>
