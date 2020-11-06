---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 2600928a21548a4af49d3d7453b04cc2c505feb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565406"
---
# <span data-ttu-id="dbe1e-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dbe1e-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="dbe1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbe1e-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe1e-103">Удаляет схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbe1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbe1e-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbe1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbe1e-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe1e-106">Командлет **Remove-AzureRmIntegrationAccountSchema** удаляет схему учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="dbe1e-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени схемы.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="dbe1e-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dbe1e-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dbe1e-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dbe1e-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dbe1e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbe1e-112">EXAMPLES</span></span>

### <span data-ttu-id="dbe1e-113">Пример 1: удаление схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="dbe1e-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="dbe1e-114">Эта команда удаляет схему учетной записи интеграции с именем IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="dbe1e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbe1e-115">PARAMETERS</span></span>

### <span data-ttu-id="dbe1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe1e-116">-DefaultProfile</span></span>
<span data-ttu-id="dbe1e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dbe1e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbe1e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dbe1e-118">-Force</span></span>
<span data-ttu-id="dbe1e-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbe1e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dbe1e-120">-Name</span></span>
<span data-ttu-id="dbe1e-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbe1e-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe1e-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dbe1e-124">-SchemaName</span></span>
<span data-ttu-id="dbe1e-125">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe1e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbe1e-126">-Confirm</span></span>
<span data-ttu-id="dbe1e-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe1e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe1e-128">-WhatIf</span></span>
<span data-ttu-id="dbe1e-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe1e-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbe1e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe1e-131">CommonParameters</span></span>
<span data-ttu-id="dbe1e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbe1e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe1e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe1e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe1e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbe1e-134">INPUTS</span></span>

### <span data-ttu-id="dbe1e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dbe1e-135">System.String</span></span>

## <span data-ttu-id="dbe1e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbe1e-136">OUTPUTS</span></span>

### <span data-ttu-id="dbe1e-137">System. void</span><span class="sxs-lookup"><span data-stu-id="dbe1e-137">System.Void</span></span>

## <span data-ttu-id="dbe1e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbe1e-138">NOTES</span></span>

## <span data-ttu-id="dbe1e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbe1e-139">RELATED LINKS</span></span>

[<span data-ttu-id="dbe1e-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dbe1e-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="dbe1e-141">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dbe1e-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="dbe1e-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dbe1e-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


