---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 44dc417521b49d47b9c060b987c82ddd06b7f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560347"
---
# <span data-ttu-id="2ad67-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2ad67-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="2ad67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ad67-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad67-103">Создание учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ad67-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ad67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ad67-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ad67-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad67-106">Командлет **New-AzureRmIntegrationAccount** создает учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ad67-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="2ad67-107">Этот командлет возвращает объект, представляющий учетную запись интеграции. Укажите имя, расположение, имя группы ресурсов и название SKU.</span><span class="sxs-lookup"><span data-stu-id="2ad67-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="2ad67-108">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="2ad67-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="2ad67-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="2ad67-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2ad67-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="2ad67-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2ad67-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="2ad67-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2ad67-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="2ad67-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2ad67-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ad67-113">EXAMPLES</span></span>

### <span data-ttu-id="2ad67-114">Пример 1: создание учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="2ad67-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="2ad67-115">Эта команда создает учетную запись интеграции с именем IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ad67-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="2ad67-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ad67-116">PARAMETERS</span></span>

### <span data-ttu-id="2ad67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad67-117">-DefaultProfile</span></span>
<span data-ttu-id="2ad67-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2ad67-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ad67-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2ad67-119">-Location</span></span>
<span data-ttu-id="2ad67-120">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ad67-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="2ad67-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ad67-121">-Name</span></span>
<span data-ttu-id="2ad67-122">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ad67-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="2ad67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad67-123">-ResourceGroupName</span></span>
<span data-ttu-id="2ad67-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ad67-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2ad67-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ad67-125">-Sku</span></span>
<span data-ttu-id="2ad67-126">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ad67-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="2ad67-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ad67-127">-Confirm</span></span>
<span data-ttu-id="2ad67-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ad67-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad67-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad67-129">-WhatIf</span></span>
<span data-ttu-id="2ad67-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ad67-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad67-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ad67-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad67-132">CommonParameters</span></span>
<span data-ttu-id="2ad67-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ad67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad67-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad67-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad67-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ad67-135">INPUTS</span></span>

### <span data-ttu-id="2ad67-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="2ad67-136">None</span></span>
<span data-ttu-id="2ad67-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2ad67-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ad67-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ad67-138">OUTPUTS</span></span>

### <span data-ttu-id="2ad67-139">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2ad67-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="2ad67-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ad67-140">NOTES</span></span>

## <span data-ttu-id="2ad67-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ad67-141">RELATED LINKS</span></span>

[<span data-ttu-id="2ad67-142">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2ad67-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="2ad67-143">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2ad67-143">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="2ad67-144">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2ad67-144">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


