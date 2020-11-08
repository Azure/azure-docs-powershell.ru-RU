---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236293"
---
# <span data-ttu-id="810a7-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="810a7-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="810a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="810a7-102">SYNOPSIS</span></span>
<span data-ttu-id="810a7-103">Удаление соглашения о учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="810a7-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="810a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="810a7-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="810a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="810a7-105">DESCRIPTION</span></span>
<span data-ttu-id="810a7-106">Командлет **Remove-AzIntegrationAccountAgreement** удаляет соглашение с учетной записью интеграции из группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="810a7-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="810a7-107">Укажите имя учетной записи интеграции, имя группы ресурсов и название соглашения.</span><span class="sxs-lookup"><span data-stu-id="810a7-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="810a7-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="810a7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="810a7-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="810a7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="810a7-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="810a7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="810a7-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="810a7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="810a7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="810a7-112">EXAMPLES</span></span>

### <span data-ttu-id="810a7-113">Пример 1: Удаление соглашения с учетной записью интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="810a7-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="810a7-114">Эта команда удаляет соглашение с учетной записью интеграции с именем IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="810a7-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="810a7-115">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="810a7-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="810a7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="810a7-116">PARAMETERS</span></span>

### <span data-ttu-id="810a7-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="810a7-117">-AgreementName</span></span>
<span data-ttu-id="810a7-118">Указывает имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="810a7-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="810a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="810a7-119">-DefaultProfile</span></span>
<span data-ttu-id="810a7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="810a7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="810a7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="810a7-121">-Force</span></span>
<span data-ttu-id="810a7-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="810a7-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="810a7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="810a7-123">-Name</span></span>
<span data-ttu-id="810a7-124">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="810a7-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="810a7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="810a7-125">-ResourceGroupName</span></span>
<span data-ttu-id="810a7-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="810a7-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="810a7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="810a7-127">-Confirm</span></span>
<span data-ttu-id="810a7-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="810a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="810a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="810a7-129">-WhatIf</span></span>
<span data-ttu-id="810a7-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="810a7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="810a7-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="810a7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="810a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="810a7-132">CommonParameters</span></span>
<span data-ttu-id="810a7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="810a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="810a7-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="810a7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="810a7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="810a7-135">INPUTS</span></span>

### <span data-ttu-id="810a7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="810a7-136">System.String</span></span>

## <span data-ttu-id="810a7-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="810a7-137">OUTPUTS</span></span>

### <span data-ttu-id="810a7-138">System. void</span><span class="sxs-lookup"><span data-stu-id="810a7-138">System.Void</span></span>

## <span data-ttu-id="810a7-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="810a7-139">NOTES</span></span>

## <span data-ttu-id="810a7-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="810a7-140">RELATED LINKS</span></span>

[<span data-ttu-id="810a7-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="810a7-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="810a7-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="810a7-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="810a7-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="810a7-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)

