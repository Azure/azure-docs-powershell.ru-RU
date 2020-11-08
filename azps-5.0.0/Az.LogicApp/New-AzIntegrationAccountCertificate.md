---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248969"
---
# <span data-ttu-id="48359-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="48359-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="48359-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48359-102">SYNOPSIS</span></span>
<span data-ttu-id="48359-103">Создание сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="48359-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="48359-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48359-104">SYNTAX</span></span>

### <span data-ttu-id="48359-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="48359-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48359-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="48359-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48359-107">Те</span><span class="sxs-lookup"><span data-stu-id="48359-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48359-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48359-108">DESCRIPTION</span></span>
<span data-ttu-id="48359-109">Командлет **New-AzIntegrationAccountCertificate** создает сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="48359-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="48359-110">Этот командлет возвращает объект, представляющий сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="48359-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="48359-111">Укажите имя учетной записи интеграции, имя группы ресурсов, имя сертификата, имя ключа, версию ключа и идентификатор хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="48359-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="48359-112">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="48359-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="48359-113">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="48359-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="48359-114">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="48359-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="48359-115">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="48359-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="48359-116">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="48359-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="48359-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48359-117">EXAMPLES</span></span>

### <span data-ttu-id="48359-118">Пример 1: создание сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="48359-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="48359-119">Эта команда создает сертификат учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48359-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="48359-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48359-120">PARAMETERS</span></span>

### <span data-ttu-id="48359-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="48359-121">-CertificateName</span></span>
<span data-ttu-id="48359-122">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="48359-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="48359-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48359-123">-DefaultProfile</span></span>
<span data-ttu-id="48359-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="48359-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48359-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="48359-125">-KeyName</span></span>
<span data-ttu-id="48359-126">Задает имя ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="48359-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48359-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="48359-127">-KeyVaultId</span></span>
<span data-ttu-id="48359-128">Указывает идентификатор хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="48359-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48359-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="48359-129">-KeyVersion</span></span>
<span data-ttu-id="48359-130">Указывает версию ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="48359-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48359-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="48359-131">-Metadata</span></span>
<span data-ttu-id="48359-132">Указывает объект метаданных для сертификата.</span><span class="sxs-lookup"><span data-stu-id="48359-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="48359-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48359-133">-Name</span></span>
<span data-ttu-id="48359-134">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="48359-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="48359-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="48359-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="48359-136">Указывает путь к общедоступному файлу сертификата (CER).</span><span class="sxs-lookup"><span data-stu-id="48359-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48359-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48359-137">-ResourceGroupName</span></span>
<span data-ttu-id="48359-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48359-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="48359-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48359-139">-Confirm</span></span>
<span data-ttu-id="48359-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48359-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48359-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48359-141">-WhatIf</span></span>
<span data-ttu-id="48359-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48359-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48359-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48359-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48359-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48359-144">CommonParameters</span></span>
<span data-ttu-id="48359-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48359-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48359-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48359-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48359-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48359-147">INPUTS</span></span>

### <span data-ttu-id="48359-148">System. String</span><span class="sxs-lookup"><span data-stu-id="48359-148">System.String</span></span>

## <span data-ttu-id="48359-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48359-149">OUTPUTS</span></span>

### <span data-ttu-id="48359-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="48359-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="48359-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="48359-151">NOTES</span></span>

## <span data-ttu-id="48359-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48359-152">RELATED LINKS</span></span>

[<span data-ttu-id="48359-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="48359-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="48359-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="48359-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="48359-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="48359-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


