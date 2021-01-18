---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504708"
---
# <span data-ttu-id="eca58-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="eca58-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="eca58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca58-102">SYNOPSIS</span></span>
<span data-ttu-id="eca58-103">Изменяет сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="eca58-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="eca58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eca58-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eca58-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eca58-105">DESCRIPTION</span></span>
<span data-ttu-id="eca58-106">**Set-AzIntegrationAccountCertificate cmdlet** изменяет сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="eca58-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="eca58-107">Этот cmdlet возвращает объект, который представляет сертификат учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="eca58-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="eca58-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="eca58-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="eca58-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="eca58-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="eca58-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="eca58-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="eca58-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="eca58-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="eca58-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="eca58-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="eca58-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eca58-113">EXAMPLES</span></span>

### <span data-ttu-id="eca58-114">Пример 1. Изменение сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="eca58-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="eca58-115">Эта команда изменяет сертификат учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eca58-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="eca58-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eca58-116">PARAMETERS</span></span>

### <span data-ttu-id="eca58-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="eca58-117">-CertificateName</span></span>
<span data-ttu-id="eca58-118">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="eca58-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="eca58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca58-119">-DefaultProfile</span></span>
<span data-ttu-id="eca58-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eca58-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eca58-121">-Force</span><span class="sxs-lookup"><span data-stu-id="eca58-121">-Force</span></span>
<span data-ttu-id="eca58-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="eca58-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eca58-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eca58-123">-KeyName</span></span>
<span data-ttu-id="eca58-124">Указывает имя ключа сертификата в хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="eca58-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="eca58-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="eca58-125">-KeyVaultId</span></span>
<span data-ttu-id="eca58-126">Определяет ИД ключа хранилища.</span><span class="sxs-lookup"><span data-stu-id="eca58-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="eca58-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="eca58-127">-KeyVersion</span></span>
<span data-ttu-id="eca58-128">Указывает версию ключа сертификата в хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="eca58-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="eca58-129">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="eca58-129">-Metadata</span></span>
<span data-ttu-id="eca58-130">Определяет объект метаданных для сертификата.</span><span class="sxs-lookup"><span data-stu-id="eca58-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="eca58-131">-Name</span><span class="sxs-lookup"><span data-stu-id="eca58-131">-Name</span></span>
<span data-ttu-id="eca58-132">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="eca58-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="eca58-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="eca58-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="eca58-134">Путь к файлу открытого сертификата (CER).</span><span class="sxs-lookup"><span data-stu-id="eca58-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="eca58-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca58-135">-ResourceGroupName</span></span>
<span data-ttu-id="eca58-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eca58-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eca58-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eca58-137">-Confirm</span></span>
<span data-ttu-id="eca58-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca58-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca58-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca58-139">-WhatIf</span></span>
<span data-ttu-id="eca58-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eca58-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca58-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eca58-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca58-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca58-142">CommonParameters</span></span>
<span data-ttu-id="eca58-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca58-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca58-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca58-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca58-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eca58-145">INPUTS</span></span>

### <span data-ttu-id="eca58-146">System.String</span><span class="sxs-lookup"><span data-stu-id="eca58-146">System.String</span></span>

## <span data-ttu-id="eca58-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eca58-147">OUTPUTS</span></span>

### <span data-ttu-id="eca58-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="eca58-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="eca58-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eca58-149">NOTES</span></span>

## <span data-ttu-id="eca58-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eca58-150">RELATED LINKS</span></span>

[<span data-ttu-id="eca58-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="eca58-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="eca58-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="eca58-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="eca58-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="eca58-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


