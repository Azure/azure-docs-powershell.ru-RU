---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 769a92f9cd164ef2b3754a84d7a948f3bedd05da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560336"
---
# <span data-ttu-id="41306-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="41306-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="41306-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41306-102">SYNOPSIS</span></span>
<span data-ttu-id="41306-103">Удаляет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="41306-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41306-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41306-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41306-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41306-105">DESCRIPTION</span></span>
<span data-ttu-id="41306-106">Командлет **Remove-AzureRmIntegrationAccountMap** удаляет карту учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41306-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="41306-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="41306-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="41306-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="41306-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="41306-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="41306-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="41306-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="41306-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="41306-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="41306-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="41306-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41306-112">EXAMPLES</span></span>

### <span data-ttu-id="41306-113">Пример 1: удаление карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="41306-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="41306-114">Эта команда удаляет карту учетной записи интеграции с именем IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="41306-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="41306-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41306-115">PARAMETERS</span></span>

### <span data-ttu-id="41306-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41306-116">-DefaultProfile</span></span>
<span data-ttu-id="41306-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="41306-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41306-118">-Force</span><span class="sxs-lookup"><span data-stu-id="41306-118">-Force</span></span>
<span data-ttu-id="41306-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="41306-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41306-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="41306-120">-MapName</span></span>
<span data-ttu-id="41306-121">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="41306-121">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="41306-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41306-122">-Name</span></span>
<span data-ttu-id="41306-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="41306-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="41306-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41306-124">-ResourceGroupName</span></span>
<span data-ttu-id="41306-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41306-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="41306-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41306-126">-Confirm</span></span>
<span data-ttu-id="41306-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41306-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41306-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41306-128">-WhatIf</span></span>
<span data-ttu-id="41306-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41306-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41306-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41306-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41306-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41306-131">CommonParameters</span></span>
<span data-ttu-id="41306-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41306-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41306-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41306-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41306-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41306-134">INPUTS</span></span>

### <span data-ttu-id="41306-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="41306-135">None</span></span>
<span data-ttu-id="41306-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="41306-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41306-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41306-137">OUTPUTS</span></span>

## <span data-ttu-id="41306-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="41306-138">NOTES</span></span>

## <span data-ttu-id="41306-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41306-139">RELATED LINKS</span></span>

[<span data-ttu-id="41306-140">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="41306-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="41306-141">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="41306-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="41306-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="41306-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


