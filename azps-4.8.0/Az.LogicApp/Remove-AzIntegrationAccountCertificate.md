---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236286"
---
# <span data-ttu-id="ed674-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ed674-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="ed674-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed674-102">SYNOPSIS</span></span>
<span data-ttu-id="ed674-103">Удаление сертификата учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed674-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="ed674-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed674-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed674-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed674-105">DESCRIPTION</span></span>
<span data-ttu-id="ed674-106">Командлет **Remove-AzIntegrationAccountCertificate** Удаляет сертификат учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed674-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="ed674-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="ed674-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="ed674-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="ed674-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ed674-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="ed674-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ed674-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="ed674-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ed674-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="ed674-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ed674-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed674-112">EXAMPLES</span></span>

### <span data-ttu-id="ed674-113">Пример 1: Удаление сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="ed674-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="ed674-114">Эта команда удаляет сертификат учетной записи интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="ed674-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="ed674-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed674-115">PARAMETERS</span></span>

### <span data-ttu-id="ed674-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ed674-116">-CertificateName</span></span>
<span data-ttu-id="ed674-117">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ed674-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="ed674-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed674-118">-DefaultProfile</span></span>
<span data-ttu-id="ed674-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed674-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed674-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ed674-120">-Force</span></span>
<span data-ttu-id="ed674-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed674-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed674-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed674-122">-Name</span></span>
<span data-ttu-id="ed674-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ed674-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ed674-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed674-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed674-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed674-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ed674-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed674-126">-Confirm</span></span>
<span data-ttu-id="ed674-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed674-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed674-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed674-128">-WhatIf</span></span>
<span data-ttu-id="ed674-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed674-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed674-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed674-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed674-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed674-131">CommonParameters</span></span>
<span data-ttu-id="ed674-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed674-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed674-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed674-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed674-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed674-134">INPUTS</span></span>

### <span data-ttu-id="ed674-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ed674-135">System.String</span></span>

## <span data-ttu-id="ed674-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed674-136">OUTPUTS</span></span>

### <span data-ttu-id="ed674-137">System. void</span><span class="sxs-lookup"><span data-stu-id="ed674-137">System.Void</span></span>

## <span data-ttu-id="ed674-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed674-138">NOTES</span></span>

## <span data-ttu-id="ed674-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed674-139">RELATED LINKS</span></span>

[<span data-ttu-id="ed674-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ed674-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ed674-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ed674-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ed674-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ed674-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)

