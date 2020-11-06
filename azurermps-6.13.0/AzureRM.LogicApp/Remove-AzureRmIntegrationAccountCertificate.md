---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 04aa8bfff795bc98b4458acb18f23535ce8bb024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564371"
---
# <span data-ttu-id="b88ee-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b88ee-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="b88ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b88ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b88ee-103">Удаление сертификата учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b88ee-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b88ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b88ee-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b88ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b88ee-105">DESCRIPTION</span></span>
<span data-ttu-id="b88ee-106">Командлет **Remove-AzureRmIntegrationAccountCertificate** Удаляет сертификат учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b88ee-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="b88ee-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="b88ee-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="b88ee-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="b88ee-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b88ee-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="b88ee-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b88ee-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="b88ee-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b88ee-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="b88ee-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b88ee-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b88ee-112">EXAMPLES</span></span>

### <span data-ttu-id="b88ee-113">Пример 1: Удаление сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="b88ee-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="b88ee-114">Эта команда удаляет сертификат учетной записи интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="b88ee-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="b88ee-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b88ee-115">PARAMETERS</span></span>

### <span data-ttu-id="b88ee-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b88ee-116">-CertificateName</span></span>
<span data-ttu-id="b88ee-117">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b88ee-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="b88ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88ee-118">-DefaultProfile</span></span>
<span data-ttu-id="b88ee-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b88ee-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88ee-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b88ee-120">-Force</span></span>
<span data-ttu-id="b88ee-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b88ee-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b88ee-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b88ee-122">-Name</span></span>
<span data-ttu-id="b88ee-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b88ee-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b88ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="b88ee-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b88ee-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b88ee-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b88ee-126">-Confirm</span></span>
<span data-ttu-id="b88ee-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b88ee-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b88ee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b88ee-128">-WhatIf</span></span>
<span data-ttu-id="b88ee-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b88ee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b88ee-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b88ee-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b88ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88ee-131">CommonParameters</span></span>
<span data-ttu-id="b88ee-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b88ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88ee-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b88ee-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88ee-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b88ee-134">INPUTS</span></span>

### <span data-ttu-id="b88ee-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b88ee-135">System.String</span></span>

## <span data-ttu-id="b88ee-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b88ee-136">OUTPUTS</span></span>

### <span data-ttu-id="b88ee-137">System. void</span><span class="sxs-lookup"><span data-stu-id="b88ee-137">System.Void</span></span>

## <span data-ttu-id="b88ee-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b88ee-138">NOTES</span></span>

## <span data-ttu-id="b88ee-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b88ee-139">RELATED LINKS</span></span>

[<span data-ttu-id="b88ee-140">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b88ee-140">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="b88ee-141">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b88ee-141">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="b88ee-142">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b88ee-142">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


