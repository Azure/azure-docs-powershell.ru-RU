---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236628"
---
# <span data-ttu-id="15a0b-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="15a0b-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="15a0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="15a0b-103">Командлеты устанавливают переход с Standard на Premium Namespace как завершенные и строки подключения в стандартном пространстве имен теперь указывают на пространство имен Premium.</span><span class="sxs-lookup"><span data-stu-id="15a0b-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="15a0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15a0b-104">SYNTAX</span></span>

### <span data-ttu-id="15a0b-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15a0b-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a0b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15a0b-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a0b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a0b-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a0b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a0b-108">DESCRIPTION</span></span>
<span data-ttu-id="15a0b-109">Командлеты **Complete-AzServiceBusMigration** устанавливают переход от стандартного к расширенному пространству имен как завершенные и строки подключения в стандартном пространстве имен теперь указывают на пространство имен Premium.</span><span class="sxs-lookup"><span data-stu-id="15a0b-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="15a0b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15a0b-110">EXAMPLES</span></span>

### <span data-ttu-id="15a0b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15a0b-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="15a0b-112">Задает миграцию пространства имен "NamespaceStandardMigration" как завершенного.</span><span class="sxs-lookup"><span data-stu-id="15a0b-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="15a0b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15a0b-113">PARAMETERS</span></span>

### <span data-ttu-id="15a0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a0b-114">-DefaultProfile</span></span>
<span data-ttu-id="15a0b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15a0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a0b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a0b-116">-InputObject</span></span>
<span data-ttu-id="15a0b-117">Настройка миграции служебной шины — стандартный объект пространства имен</span><span class="sxs-lookup"><span data-stu-id="15a0b-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="15a0b-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15a0b-118">-Name</span></span>
<span data-ttu-id="15a0b-119">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="15a0b-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="15a0b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15a0b-120">-PassThru</span></span>
<span data-ttu-id="15a0b-121">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="15a0b-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="15a0b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a0b-122">-ResourceGroupName</span></span>
<span data-ttu-id="15a0b-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="15a0b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="15a0b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a0b-124">-ResourceId</span></span>
<span data-ttu-id="15a0b-125">Миграция служебной шины — идентификатор стандартных ресурсов пространства имен</span><span class="sxs-lookup"><span data-stu-id="15a0b-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="15a0b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15a0b-126">-Confirm</span></span>
<span data-ttu-id="15a0b-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15a0b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a0b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a0b-128">-WhatIf</span></span>
<span data-ttu-id="15a0b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15a0b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a0b-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15a0b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a0b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a0b-131">CommonParameters</span></span>
<span data-ttu-id="15a0b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15a0b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a0b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a0b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a0b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15a0b-134">INPUTS</span></span>

### <span data-ttu-id="15a0b-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="15a0b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="15a0b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="15a0b-136">System.String</span></span>

## <span data-ttu-id="15a0b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a0b-137">OUTPUTS</span></span>

### <span data-ttu-id="15a0b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15a0b-138">System.Boolean</span></span>

## <span data-ttu-id="15a0b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="15a0b-139">NOTES</span></span>

## <span data-ttu-id="15a0b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15a0b-140">RELATED LINKS</span></span>
