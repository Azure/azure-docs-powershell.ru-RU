---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: a0ffbc31727b7267be59b9645d99abdce1bfeae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563456"
---
# <span data-ttu-id="62861-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="62861-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="62861-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62861-102">SYNOPSIS</span></span>
<span data-ttu-id="62861-103">Изменение сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="62861-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62861-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62861-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62861-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62861-105">DESCRIPTION</span></span>
<span data-ttu-id="62861-106">Командлет **Set-AzureRmIntegrationAccountCertificate** изменяет сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="62861-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="62861-107">Этот командлет возвращает объект, представляющий сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="62861-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="62861-108">Указание имени учетной записи интеграции, имени группы ресурсов и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="62861-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="62861-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="62861-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="62861-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="62861-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="62861-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="62861-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="62861-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="62861-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="62861-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62861-113">EXAMPLES</span></span>

### <span data-ttu-id="62861-114">Пример 1: изменение сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="62861-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
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

<span data-ttu-id="62861-115">Эта команда изменяет сертификат учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62861-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="62861-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62861-116">PARAMETERS</span></span>

### <span data-ttu-id="62861-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="62861-117">-CertificateName</span></span>
<span data-ttu-id="62861-118">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="62861-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="62861-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62861-119">-DefaultProfile</span></span>
<span data-ttu-id="62861-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62861-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62861-121">-Force</span><span class="sxs-lookup"><span data-stu-id="62861-121">-Force</span></span>
<span data-ttu-id="62861-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="62861-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62861-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="62861-123">-KeyName</span></span>
<span data-ttu-id="62861-124">Задает имя ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="62861-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62861-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="62861-125">-KeyVaultId</span></span>
<span data-ttu-id="62861-126">Указывает идентификатор хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="62861-126">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62861-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="62861-127">-KeyVersion</span></span>
<span data-ttu-id="62861-128">Указывает версию ключа сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="62861-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62861-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="62861-129">-Metadata</span></span>
<span data-ttu-id="62861-130">Указывает объект метаданных для сертификата.</span><span class="sxs-lookup"><span data-stu-id="62861-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="62861-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62861-131">-Name</span></span>
<span data-ttu-id="62861-132">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="62861-132">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62861-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="62861-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="62861-134">Указывает путь к общедоступному файлу сертификата (CER).</span><span class="sxs-lookup"><span data-stu-id="62861-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62861-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62861-135">-ResourceGroupName</span></span>
<span data-ttu-id="62861-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62861-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="62861-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62861-137">-Confirm</span></span>
<span data-ttu-id="62861-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62861-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62861-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62861-139">-WhatIf</span></span>
<span data-ttu-id="62861-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62861-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62861-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62861-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62861-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62861-142">CommonParameters</span></span>
<span data-ttu-id="62861-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62861-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62861-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62861-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62861-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62861-145">INPUTS</span></span>

### <span data-ttu-id="62861-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="62861-146">None</span></span>
<span data-ttu-id="62861-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="62861-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62861-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62861-148">OUTPUTS</span></span>

### <span data-ttu-id="62861-149">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="62861-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="62861-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="62861-150">NOTES</span></span>

## <span data-ttu-id="62861-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62861-151">RELATED LINKS</span></span>

[<span data-ttu-id="62861-152">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="62861-152">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="62861-153">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="62861-153">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="62861-154">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="62861-154">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


