---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: ba5614777153c5e70242992b39aadc96a37ed865
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899845"
---
# <span data-ttu-id="028a9-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="028a9-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="028a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="028a9-102">SYNOPSIS</span></span>
<span data-ttu-id="028a9-103">Изменение сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="028a9-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="028a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="028a9-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="028a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="028a9-105">DESCRIPTION</span></span>
<span data-ttu-id="028a9-106">Командлет **Set-AzIntegrationAccountCertificate** изменяет сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="028a9-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="028a9-107">Этот командлет возвращает объект, представляющий сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="028a9-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="028a9-108">Указание имени учетной записи интеграции, имени группы ресурсов и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="028a9-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="028a9-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="028a9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="028a9-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="028a9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="028a9-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="028a9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="028a9-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="028a9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="028a9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="028a9-113">EXAMPLES</span></span>

### <span data-ttu-id="028a9-114">Пример 1: изменение сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="028a9-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="028a9-115">Эта команда изменяет сертификат учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="028a9-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="028a9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="028a9-116">PARAMETERS</span></span>

### <span data-ttu-id="028a9-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="028a9-117">-CertificateName</span></span>
<span data-ttu-id="028a9-118">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="028a9-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="028a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028a9-119">-DefaultProfile</span></span>
<span data-ttu-id="028a9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="028a9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="028a9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="028a9-121">-Force</span></span>
<span data-ttu-id="028a9-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="028a9-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="028a9-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="028a9-123">-KeyName</span></span>
<span data-ttu-id="028a9-124">Задает имя ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="028a9-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028a9-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="028a9-125">-KeyVaultId</span></span>
<span data-ttu-id="028a9-126">Указывает идентификатор хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="028a9-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028a9-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="028a9-127">-KeyVersion</span></span>
<span data-ttu-id="028a9-128">Указывает версию ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="028a9-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028a9-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="028a9-129">-Metadata</span></span>
<span data-ttu-id="028a9-130">Указывает объект метаданных для сертификата.</span><span class="sxs-lookup"><span data-stu-id="028a9-130">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028a9-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="028a9-131">-Name</span></span>
<span data-ttu-id="028a9-132">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="028a9-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028a9-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="028a9-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="028a9-134">Указывает путь к общедоступному файлу сертификата (CER).</span><span class="sxs-lookup"><span data-stu-id="028a9-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="028a9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="028a9-135">-ResourceGroupName</span></span>
<span data-ttu-id="028a9-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="028a9-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="028a9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="028a9-137">-Confirm</span></span>
<span data-ttu-id="028a9-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="028a9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="028a9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="028a9-139">-WhatIf</span></span>
<span data-ttu-id="028a9-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="028a9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="028a9-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="028a9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="028a9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028a9-142">CommonParameters</span></span>
<span data-ttu-id="028a9-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="028a9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028a9-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="028a9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028a9-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="028a9-145">INPUTS</span></span>

### <span data-ttu-id="028a9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="028a9-146">System.String</span></span>

## <span data-ttu-id="028a9-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="028a9-147">OUTPUTS</span></span>

### <span data-ttu-id="028a9-148">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="028a9-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="028a9-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="028a9-149">NOTES</span></span>

## <span data-ttu-id="028a9-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="028a9-150">RELATED LINKS</span></span>

[<span data-ttu-id="028a9-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="028a9-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="028a9-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="028a9-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="028a9-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="028a9-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


