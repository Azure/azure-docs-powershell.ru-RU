---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: cd15a6f132360bba973e9361cf2f6e98c9bf24f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968936"
---
# <span data-ttu-id="6b821-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6b821-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="6b821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b821-102">SYNOPSIS</span></span>
<span data-ttu-id="6b821-103">Удаляет соглашение об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="6b821-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="6b821-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b821-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b821-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b821-105">DESCRIPTION</span></span>
<span data-ttu-id="6b821-106">С **его использованием** из группы ресурсов Azure удаляется соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6b821-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="6b821-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя соглашения.</span><span class="sxs-lookup"><span data-stu-id="6b821-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="6b821-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="6b821-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6b821-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="6b821-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6b821-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="6b821-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6b821-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="6b821-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6b821-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b821-112">EXAMPLES</span></span>

### <span data-ttu-id="6b821-113">Пример 1. Удаление соглашения об учетной записи интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="6b821-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="6b821-114">Эта команда удаляет соглашение об учетной записи интеграции IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="6b821-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="6b821-115">Команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6b821-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6b821-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b821-116">PARAMETERS</span></span>

### <span data-ttu-id="6b821-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6b821-117">-AgreementName</span></span>
<span data-ttu-id="6b821-118">Указывает имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6b821-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="6b821-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b821-119">-DefaultProfile</span></span>
<span data-ttu-id="6b821-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b821-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b821-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6b821-121">-Force</span></span>
<span data-ttu-id="6b821-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6b821-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b821-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6b821-123">-Name</span></span>
<span data-ttu-id="6b821-124">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6b821-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="6b821-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b821-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b821-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b821-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6b821-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b821-127">-Confirm</span></span>
<span data-ttu-id="6b821-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b821-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b821-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b821-129">-WhatIf</span></span>
<span data-ttu-id="6b821-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b821-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b821-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6b821-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b821-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b821-132">CommonParameters</span></span>
<span data-ttu-id="6b821-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b821-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b821-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b821-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b821-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b821-135">INPUTS</span></span>

### <span data-ttu-id="6b821-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6b821-136">System.String</span></span>

## <span data-ttu-id="6b821-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b821-137">OUTPUTS</span></span>

### <span data-ttu-id="6b821-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="6b821-138">System.Void</span></span>

## <span data-ttu-id="6b821-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b821-139">NOTES</span></span>

## <span data-ttu-id="6b821-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b821-140">RELATED LINKS</span></span>

[<span data-ttu-id="6b821-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6b821-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6b821-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6b821-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="6b821-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6b821-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


