---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414004"
---
# <span data-ttu-id="50147-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="50147-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="50147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50147-102">SYNOPSIS</span></span>
<span data-ttu-id="50147-103">Удаляет соглашение об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="50147-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="50147-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50147-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50147-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50147-105">DESCRIPTION</span></span>
<span data-ttu-id="50147-106">С **его использованием** из группы ресурсов Azure удаляется соглашение об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="50147-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="50147-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя соглашения.</span><span class="sxs-lookup"><span data-stu-id="50147-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="50147-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="50147-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="50147-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="50147-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="50147-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="50147-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="50147-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="50147-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="50147-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50147-112">EXAMPLES</span></span>

### <span data-ttu-id="50147-113">Пример 1. Удаление соглашения об учетной записи интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="50147-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="50147-114">Эта команда удаляет соглашение об учетной записи интеграции IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="50147-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="50147-115">Команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="50147-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="50147-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50147-116">PARAMETERS</span></span>

### <span data-ttu-id="50147-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="50147-117">-AgreementName</span></span>
<span data-ttu-id="50147-118">Указывает имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="50147-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="50147-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50147-119">-DefaultProfile</span></span>
<span data-ttu-id="50147-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="50147-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50147-121">-Force</span><span class="sxs-lookup"><span data-stu-id="50147-121">-Force</span></span>
<span data-ttu-id="50147-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="50147-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50147-123">-Name</span><span class="sxs-lookup"><span data-stu-id="50147-123">-Name</span></span>
<span data-ttu-id="50147-124">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="50147-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="50147-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50147-125">-ResourceGroupName</span></span>
<span data-ttu-id="50147-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50147-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="50147-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50147-127">-Confirm</span></span>
<span data-ttu-id="50147-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50147-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50147-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50147-129">-WhatIf</span></span>
<span data-ttu-id="50147-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50147-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50147-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50147-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50147-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50147-132">CommonParameters</span></span>
<span data-ttu-id="50147-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50147-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50147-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50147-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50147-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50147-135">INPUTS</span></span>

### <span data-ttu-id="50147-136">System.String</span><span class="sxs-lookup"><span data-stu-id="50147-136">System.String</span></span>

## <span data-ttu-id="50147-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50147-137">OUTPUTS</span></span>

### <span data-ttu-id="50147-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="50147-138">System.Void</span></span>

## <span data-ttu-id="50147-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50147-139">NOTES</span></span>

## <span data-ttu-id="50147-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50147-140">RELATED LINKS</span></span>

[<span data-ttu-id="50147-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="50147-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="50147-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="50147-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="50147-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="50147-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


