---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406999"
---
# <span data-ttu-id="e313e-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e313e-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e313e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e313e-102">SYNOPSIS</span></span>
<span data-ttu-id="e313e-103">Создание сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e313e-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="e313e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e313e-104">SYNTAX</span></span>

### <span data-ttu-id="e313e-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="e313e-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e313e-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="e313e-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e313e-107">И то, и другое</span><span class="sxs-lookup"><span data-stu-id="e313e-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e313e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e313e-108">DESCRIPTION</span></span>
<span data-ttu-id="e313e-109">**Новый-AzIntegrationAccountCertificate** создает сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e313e-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="e313e-110">Этот cmdlet возвращает объект, который представляет сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e313e-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="e313e-111">Укажите имя учетной записи интеграции, имя группы ресурсов, имя сертификата, имя ключа, версию ключа и ИД хранилища ключа.</span><span class="sxs-lookup"><span data-stu-id="e313e-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="e313e-112">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="e313e-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="e313e-113">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e313e-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e313e-114">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="e313e-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e313e-115">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="e313e-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e313e-116">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="e313e-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e313e-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e313e-117">EXAMPLES</span></span>

### <span data-ttu-id="e313e-118">Пример 1. Создание сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="e313e-118">Example 1: Create an integration account certificate</span></span>
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

<span data-ttu-id="e313e-119">Эта команда создает сертификат учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e313e-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="e313e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e313e-120">PARAMETERS</span></span>

### <span data-ttu-id="e313e-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e313e-121">-CertificateName</span></span>
<span data-ttu-id="e313e-122">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e313e-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="e313e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e313e-123">-DefaultProfile</span></span>
<span data-ttu-id="e313e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e313e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e313e-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e313e-125">-KeyName</span></span>
<span data-ttu-id="e313e-126">Указывает имя ключа сертификата в хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="e313e-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e313e-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e313e-127">-KeyVaultId</span></span>
<span data-ttu-id="e313e-128">Определяет ИД ключа хранилища.</span><span class="sxs-lookup"><span data-stu-id="e313e-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="e313e-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="e313e-129">-KeyVersion</span></span>
<span data-ttu-id="e313e-130">Указывает версию ключа сертификата в хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="e313e-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e313e-131">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="e313e-131">-Metadata</span></span>
<span data-ttu-id="e313e-132">Определяет объект метаданных для сертификата.</span><span class="sxs-lookup"><span data-stu-id="e313e-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="e313e-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e313e-133">-Name</span></span>
<span data-ttu-id="e313e-134">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e313e-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="e313e-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e313e-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="e313e-136">Путь к файлу открытого сертификата (CER).</span><span class="sxs-lookup"><span data-stu-id="e313e-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="e313e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e313e-137">-ResourceGroupName</span></span>
<span data-ttu-id="e313e-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e313e-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e313e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e313e-139">-Confirm</span></span>
<span data-ttu-id="e313e-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e313e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e313e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e313e-141">-WhatIf</span></span>
<span data-ttu-id="e313e-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e313e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e313e-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e313e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e313e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e313e-144">CommonParameters</span></span>
<span data-ttu-id="e313e-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e313e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e313e-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e313e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e313e-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e313e-147">INPUTS</span></span>

### <span data-ttu-id="e313e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e313e-148">System.String</span></span>

## <span data-ttu-id="e313e-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e313e-149">OUTPUTS</span></span>

### <span data-ttu-id="e313e-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e313e-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="e313e-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e313e-151">NOTES</span></span>

## <span data-ttu-id="e313e-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e313e-152">RELATED LINKS</span></span>

[<span data-ttu-id="e313e-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e313e-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e313e-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e313e-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e313e-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e313e-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


