---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 29eb57e7c076499f105bec9e2400091ac11b09fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560339"
---
# <span data-ttu-id="e5f16-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e5f16-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="e5f16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5f16-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f16-103">Удаление партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e5f16-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5f16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5f16-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5f16-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f16-106">Командлет **Remove-AzureRmIntegrationAccountPartner** удаляет партнера учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5f16-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="e5f16-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="e5f16-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="e5f16-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e5f16-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e5f16-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="e5f16-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e5f16-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="e5f16-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e5f16-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="e5f16-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e5f16-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5f16-112">EXAMPLES</span></span>

### <span data-ttu-id="e5f16-113">Пример 1: Удаление партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="e5f16-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="e5f16-114">Эта команда удаляет партнера учетной записи интеграции с именем IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="e5f16-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="e5f16-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5f16-115">PARAMETERS</span></span>

### <span data-ttu-id="e5f16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f16-116">-DefaultProfile</span></span>
<span data-ttu-id="e5f16-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5f16-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5f16-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e5f16-118">-Force</span></span>
<span data-ttu-id="e5f16-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e5f16-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5f16-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5f16-120">-Name</span></span>
<span data-ttu-id="e5f16-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e5f16-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="e5f16-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="e5f16-122">-PartnerName</span></span>
<span data-ttu-id="e5f16-123">Указывает имя партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e5f16-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="e5f16-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f16-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5f16-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5f16-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5f16-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5f16-126">-Confirm</span></span>
<span data-ttu-id="e5f16-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5f16-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f16-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f16-128">-WhatIf</span></span>
<span data-ttu-id="e5f16-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5f16-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f16-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5f16-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f16-131">CommonParameters</span></span>
<span data-ttu-id="e5f16-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5f16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f16-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f16-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f16-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5f16-134">INPUTS</span></span>

### <span data-ttu-id="e5f16-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="e5f16-135">None</span></span>
<span data-ttu-id="e5f16-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e5f16-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5f16-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5f16-137">OUTPUTS</span></span>

## <span data-ttu-id="e5f16-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5f16-138">NOTES</span></span>

## <span data-ttu-id="e5f16-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5f16-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5f16-140">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e5f16-140">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="e5f16-141">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e5f16-141">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="e5f16-142">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e5f16-142">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


