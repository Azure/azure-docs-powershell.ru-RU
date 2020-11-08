---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246178"
---
# <span data-ttu-id="fbb45-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fbb45-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="fbb45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbb45-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb45-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="fbb45-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="fbb45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbb45-104">SYNTAX</span></span>

### <span data-ttu-id="fbb45-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbb45-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb45-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fbb45-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb45-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb45-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb45-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb45-108">DESCRIPTION</span></span>
<span data-ttu-id="fbb45-109">Командлеты **Stop-AzServiceBusMigration** прерывает миграцию между стандартным и расширенным пространством имен</span><span class="sxs-lookup"><span data-stu-id="fbb45-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="fbb45-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbb45-110">EXAMPLES</span></span>

### <span data-ttu-id="fbb45-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbb45-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="fbb45-112">Командлет завершает миграцию между стандартным пространством имен и пространством имен Premium, указанным при создании конфигурации миграции.</span><span class="sxs-lookup"><span data-stu-id="fbb45-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="fbb45-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbb45-113">PARAMETERS</span></span>

### <span data-ttu-id="fbb45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb45-114">-DefaultProfile</span></span>
<span data-ttu-id="fbb45-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb45-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb45-116">-InputObject</span></span>
<span data-ttu-id="fbb45-117">Объект стандартного пространства имен для настройки миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="fbb45-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="fbb45-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbb45-118">-Name</span></span>
<span data-ttu-id="fbb45-119">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="fbb45-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="fbb45-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbb45-120">-PassThru</span></span>
<span data-ttu-id="fbb45-121">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fbb45-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fbb45-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb45-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbb45-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fbb45-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fbb45-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb45-124">-ResourceId</span></span>
<span data-ttu-id="fbb45-125">Идентификатор ресурса стандартного пространства имен для настройки миграции служебной шины</span><span class="sxs-lookup"><span data-stu-id="fbb45-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="fbb45-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb45-126">-Confirm</span></span>
<span data-ttu-id="fbb45-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbb45-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb45-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb45-128">-WhatIf</span></span>
<span data-ttu-id="fbb45-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbb45-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb45-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbb45-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb45-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb45-131">CommonParameters</span></span>
<span data-ttu-id="fbb45-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbb45-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb45-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb45-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb45-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbb45-134">INPUTS</span></span>

### <span data-ttu-id="fbb45-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fbb45-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="fbb45-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb45-136">System.String</span></span>

## <span data-ttu-id="fbb45-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb45-137">OUTPUTS</span></span>

### <span data-ttu-id="fbb45-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb45-138">System.Boolean</span></span>

## <span data-ttu-id="fbb45-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbb45-139">NOTES</span></span>

## <span data-ttu-id="fbb45-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbb45-140">RELATED LINKS</span></span>
