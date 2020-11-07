---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 88661e132e6f40f4bb8e90fac339ddf1946085c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732852"
---
# <span data-ttu-id="a55c5-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a55c5-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="a55c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a55c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a55c5-103">Удаление соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a55c5-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a55c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a55c5-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a55c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55c5-105">DESCRIPTION</span></span>
<span data-ttu-id="a55c5-106">Командлет **Remove-AzureRmIntegrationAccountAgreement** удаляет соглашение с учетной записью интеграции из группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a55c5-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="a55c5-107">Укажите имя учетной записи интеграции, имя группы ресурсов и название соглашения.</span><span class="sxs-lookup"><span data-stu-id="a55c5-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="a55c5-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a55c5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a55c5-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a55c5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a55c5-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a55c5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a55c5-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a55c5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a55c5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a55c5-112">EXAMPLES</span></span>

### <span data-ttu-id="a55c5-113">Пример 1: Удаление соглашения с учетной записью интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="a55c5-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="a55c5-114">Эта команда удаляет соглашение с учетной записью интеграции с именем IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="a55c5-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="a55c5-115">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a55c5-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a55c5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a55c5-116">PARAMETERS</span></span>

### <span data-ttu-id="a55c5-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="a55c5-117">-AgreementName</span></span>
<span data-ttu-id="a55c5-118">Указывает имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a55c5-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="a55c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55c5-119">-DefaultProfile</span></span>
<span data-ttu-id="a55c5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a55c5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a55c5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a55c5-121">-Force</span></span>
<span data-ttu-id="a55c5-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a55c5-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a55c5-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a55c5-123">-Name</span></span>
<span data-ttu-id="a55c5-124">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a55c5-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="a55c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a55c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a55c5-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a55c5-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a55c5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a55c5-127">-Confirm</span></span>
<span data-ttu-id="a55c5-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a55c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a55c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a55c5-129">-WhatIf</span></span>
<span data-ttu-id="a55c5-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a55c5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a55c5-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a55c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a55c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55c5-132">CommonParameters</span></span>
<span data-ttu-id="a55c5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a55c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55c5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55c5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55c5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a55c5-135">INPUTS</span></span>

### <span data-ttu-id="a55c5-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="a55c5-136">None</span></span>
<span data-ttu-id="a55c5-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a55c5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a55c5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55c5-138">OUTPUTS</span></span>

## <span data-ttu-id="a55c5-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a55c5-139">NOTES</span></span>

## <span data-ttu-id="a55c5-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a55c5-140">RELATED LINKS</span></span>

[<span data-ttu-id="a55c5-141">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a55c5-141">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="a55c5-142">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a55c5-142">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="a55c5-143">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="a55c5-143">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


