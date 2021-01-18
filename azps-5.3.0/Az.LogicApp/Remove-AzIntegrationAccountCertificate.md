---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507159"
---
# <span data-ttu-id="52aab-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="52aab-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="52aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52aab-102">SYNOPSIS</span></span>
<span data-ttu-id="52aab-103">Удаляет сертификат учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52aab-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="52aab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52aab-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52aab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52aab-105">DESCRIPTION</span></span>
<span data-ttu-id="52aab-106">При **этом из группы** ресурсов удаляется сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="52aab-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="52aab-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="52aab-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="52aab-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="52aab-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="52aab-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="52aab-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="52aab-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="52aab-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="52aab-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="52aab-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="52aab-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52aab-112">EXAMPLES</span></span>

### <span data-ttu-id="52aab-113">Пример 1. Удаление сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="52aab-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="52aab-114">Эта команда удаляет сертификат учетной записи интеграции IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="52aab-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="52aab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52aab-115">PARAMETERS</span></span>

### <span data-ttu-id="52aab-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="52aab-116">-CertificateName</span></span>
<span data-ttu-id="52aab-117">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="52aab-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="52aab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52aab-118">-DefaultProfile</span></span>
<span data-ttu-id="52aab-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="52aab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52aab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="52aab-120">-Force</span></span>
<span data-ttu-id="52aab-121">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="52aab-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52aab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="52aab-122">-Name</span></span>
<span data-ttu-id="52aab-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="52aab-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="52aab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52aab-124">-ResourceGroupName</span></span>
<span data-ttu-id="52aab-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52aab-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="52aab-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52aab-126">-Confirm</span></span>
<span data-ttu-id="52aab-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="52aab-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52aab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52aab-128">-WhatIf</span></span>
<span data-ttu-id="52aab-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52aab-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52aab-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="52aab-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52aab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52aab-131">CommonParameters</span></span>
<span data-ttu-id="52aab-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52aab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52aab-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52aab-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52aab-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52aab-134">INPUTS</span></span>

### <span data-ttu-id="52aab-135">System.String</span><span class="sxs-lookup"><span data-stu-id="52aab-135">System.String</span></span>

## <span data-ttu-id="52aab-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52aab-136">OUTPUTS</span></span>

### <span data-ttu-id="52aab-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="52aab-137">System.Void</span></span>

## <span data-ttu-id="52aab-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52aab-138">NOTES</span></span>

## <span data-ttu-id="52aab-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52aab-139">RELATED LINKS</span></span>

[<span data-ttu-id="52aab-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="52aab-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="52aab-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="52aab-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="52aab-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="52aab-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


