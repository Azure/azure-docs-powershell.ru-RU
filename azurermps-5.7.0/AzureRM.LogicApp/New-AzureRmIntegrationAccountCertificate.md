---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 555da1343813884a1f773d199cb99a188f7efedc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566619"
---
# <span data-ttu-id="3957c-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3957c-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="3957c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3957c-102">SYNOPSIS</span></span>
<span data-ttu-id="3957c-103">Создание сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3957c-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3957c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3957c-104">SYNTAX</span></span>

### <span data-ttu-id="3957c-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="3957c-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3957c-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="3957c-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3957c-107">Те</span><span class="sxs-lookup"><span data-stu-id="3957c-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3957c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3957c-108">DESCRIPTION</span></span>
<span data-ttu-id="3957c-109">Командлет **New-AzureRmIntegrationAccountCertificate** создает сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3957c-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="3957c-110">Этот командлет возвращает объект, представляющий сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3957c-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="3957c-111">Укажите имя учетной записи интеграции, имя группы ресурсов, имя сертификата, имя ключа, версию ключа и идентификатор хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3957c-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="3957c-112">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="3957c-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="3957c-113">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="3957c-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3957c-114">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="3957c-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3957c-115">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="3957c-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3957c-116">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="3957c-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3957c-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3957c-117">EXAMPLES</span></span>

### <span data-ttu-id="3957c-118">Пример 1: создание сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="3957c-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="3957c-119">Эта команда создает сертификат учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3957c-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="3957c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3957c-120">PARAMETERS</span></span>

### <span data-ttu-id="3957c-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3957c-121">-CertificateName</span></span>
<span data-ttu-id="3957c-122">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3957c-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="3957c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3957c-123">-DefaultProfile</span></span>
<span data-ttu-id="3957c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3957c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3957c-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3957c-125">-KeyName</span></span>
<span data-ttu-id="3957c-126">Задает имя ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3957c-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3957c-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="3957c-127">-KeyVaultId</span></span>
<span data-ttu-id="3957c-128">Указывает идентификатор хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3957c-128">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3957c-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="3957c-129">-KeyVersion</span></span>
<span data-ttu-id="3957c-130">Указывает версию ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3957c-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3957c-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3957c-131">-Metadata</span></span>
<span data-ttu-id="3957c-132">Указывает объект метаданных для сертификата.</span><span class="sxs-lookup"><span data-stu-id="3957c-132">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3957c-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3957c-133">-Name</span></span>
<span data-ttu-id="3957c-134">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3957c-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3957c-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3957c-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="3957c-136">Указывает путь к общедоступному файлу сертификата (CER).</span><span class="sxs-lookup"><span data-stu-id="3957c-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3957c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3957c-137">-ResourceGroupName</span></span>
<span data-ttu-id="3957c-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3957c-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3957c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3957c-139">-Confirm</span></span>
<span data-ttu-id="3957c-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3957c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3957c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3957c-141">-WhatIf</span></span>
<span data-ttu-id="3957c-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3957c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3957c-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3957c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3957c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3957c-144">CommonParameters</span></span>
<span data-ttu-id="3957c-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3957c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3957c-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3957c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3957c-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3957c-147">INPUTS</span></span>

### <span data-ttu-id="3957c-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="3957c-148">None</span></span>
<span data-ttu-id="3957c-149">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3957c-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3957c-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3957c-150">OUTPUTS</span></span>

### <span data-ttu-id="3957c-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3957c-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="3957c-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="3957c-152">NOTES</span></span>

## <span data-ttu-id="3957c-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3957c-153">RELATED LINKS</span></span>

[<span data-ttu-id="3957c-154">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3957c-154">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="3957c-155">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3957c-155">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="3957c-156">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3957c-156">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


