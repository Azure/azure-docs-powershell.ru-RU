---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a1a34ca669b12ee815655531c33b6cdba519016c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734704"
---
# <span data-ttu-id="319af-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="319af-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="319af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="319af-102">SYNOPSIS</span></span>
<span data-ttu-id="319af-103">Удаляет схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="319af-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="319af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="319af-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="319af-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="319af-105">DESCRIPTION</span></span>
<span data-ttu-id="319af-106">Командлет **Remove-AzureRmIntegrationAccountSchema** удаляет схему учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="319af-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="319af-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени схемы.</span><span class="sxs-lookup"><span data-stu-id="319af-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="319af-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="319af-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="319af-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="319af-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="319af-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="319af-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="319af-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="319af-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="319af-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="319af-112">EXAMPLES</span></span>

### <span data-ttu-id="319af-113">Пример 1: удаление схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="319af-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="319af-114">Эта команда удаляет схему учетной записи интеграции с именем IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="319af-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="319af-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="319af-115">PARAMETERS</span></span>

### <span data-ttu-id="319af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319af-116">-DefaultProfile</span></span>
<span data-ttu-id="319af-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="319af-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="319af-118">-Force</span></span>
<span data-ttu-id="319af-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="319af-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319af-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="319af-120">-Name</span></span>
<span data-ttu-id="319af-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="319af-121">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319af-122">-ResourceGroupName</span></span>
<span data-ttu-id="319af-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="319af-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319af-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="319af-124">-SchemaName</span></span>
<span data-ttu-id="319af-125">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="319af-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319af-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="319af-126">-Confirm</span></span>
<span data-ttu-id="319af-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="319af-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319af-128">-WhatIf</span></span>
<span data-ttu-id="319af-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="319af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="319af-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="319af-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319af-131">CommonParameters</span></span>
<span data-ttu-id="319af-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="319af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319af-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="319af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319af-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="319af-134">INPUTS</span></span>

### <span data-ttu-id="319af-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="319af-135">None</span></span>
<span data-ttu-id="319af-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="319af-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="319af-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="319af-137">OUTPUTS</span></span>

## <span data-ttu-id="319af-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="319af-138">NOTES</span></span>

## <span data-ttu-id="319af-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="319af-139">RELATED LINKS</span></span>

[<span data-ttu-id="319af-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="319af-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="319af-141">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="319af-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="319af-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="319af-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


