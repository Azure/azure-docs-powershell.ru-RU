---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: d2948378f9312687e2dbbe09bd7c583cbe085778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563459"
---
# <span data-ttu-id="978f1-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="978f1-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="978f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="978f1-102">SYNOPSIS</span></span>
<span data-ttu-id="978f1-103">Изменение учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="978f1-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="978f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="978f1-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="978f1-105">DESCRIPTION</span></span>
<span data-ttu-id="978f1-106">Командлет **Set-AzureRmIntegrationAccount** изменяет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="978f1-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="978f1-107">Этот командлет возвращает объект, представляющий учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="978f1-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="978f1-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="978f1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="978f1-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="978f1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="978f1-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="978f1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="978f1-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="978f1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="978f1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="978f1-112">EXAMPLES</span></span>

### <span data-ttu-id="978f1-113">Пример 1: изменение учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="978f1-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="978f1-114">Эта команда изменяет учетную запись интеграции с именем IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="978f1-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="978f1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="978f1-115">PARAMETERS</span></span>

### <span data-ttu-id="978f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978f1-116">-DefaultProfile</span></span>
<span data-ttu-id="978f1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="978f1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="978f1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="978f1-118">-Force</span></span>
<span data-ttu-id="978f1-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="978f1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="978f1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="978f1-120">-Location</span></span>
<span data-ttu-id="978f1-121">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="978f1-121">Specifies a location for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978f1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="978f1-122">-Name</span></span>
<span data-ttu-id="978f1-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="978f1-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="978f1-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="978f1-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="978f1-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="978f1-126">-Sku</span></span>
<span data-ttu-id="978f1-127">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="978f1-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978f1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="978f1-128">-Confirm</span></span>
<span data-ttu-id="978f1-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="978f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978f1-130">-WhatIf</span></span>
<span data-ttu-id="978f1-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="978f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978f1-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="978f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978f1-133">CommonParameters</span></span>
<span data-ttu-id="978f1-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="978f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978f1-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="978f1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978f1-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="978f1-136">INPUTS</span></span>

### <span data-ttu-id="978f1-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="978f1-137">None</span></span>
<span data-ttu-id="978f1-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="978f1-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="978f1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="978f1-139">OUTPUTS</span></span>

### <span data-ttu-id="978f1-140">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="978f1-140">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="978f1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="978f1-141">NOTES</span></span>

## <span data-ttu-id="978f1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="978f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="978f1-143">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="978f1-143">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="978f1-144">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="978f1-144">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="978f1-145">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="978f1-145">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


