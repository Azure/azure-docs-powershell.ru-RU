---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: fdb90d670034e87c4a08c316b73d4bd15614d872
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720620"
---
# <span data-ttu-id="3db2f-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3db2f-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3db2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3db2f-102">SYNOPSIS</span></span>
<span data-ttu-id="3db2f-103">Задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3db2f-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="3db2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3db2f-104">SYNTAX</span></span>

### <span data-ttu-id="3db2f-105">Развернуто (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3db2f-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db2f-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="3db2f-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db2f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3db2f-107">DESCRIPTION</span></span>
<span data-ttu-id="3db2f-108">Командлет Set-AzKeyVaultCertificateIssuer задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3db2f-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="3db2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3db2f-109">EXAMPLES</span></span>

### <span data-ttu-id="3db2f-110">Пример 1: Настройка поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="3db2f-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="3db2f-111">Эта команда задает свойства для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="3db2f-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="3db2f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3db2f-112">PARAMETERS</span></span>

### <span data-ttu-id="3db2f-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="3db2f-113">-AccountId</span></span>
<span data-ttu-id="3db2f-114">Указывает идентификатор учетной записи для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="3db2f-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="3db2f-115">-ApiKey</span></span>
<span data-ttu-id="3db2f-116">Указывает ключ API для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="3db2f-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db2f-117">-DefaultProfile</span></span>
<span data-ttu-id="3db2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3db2f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3db2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3db2f-119">-InputObject</span></span>
<span data-ttu-id="3db2f-120">Указывает издателя сертификата, который нужно задать.</span><span class="sxs-lookup"><span data-stu-id="3db2f-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="3db2f-121">-IssuerProvider</span></span>
<span data-ttu-id="3db2f-122">Указывает тип заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="3db2f-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3db2f-123">-Name</span></span>
<span data-ttu-id="3db2f-124">Указывает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="3db2f-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3db2f-125">-OrganizationDetails</span></span>
<span data-ttu-id="3db2f-126">Сведения об организации, которые будут использоваться для поставщика.</span><span class="sxs-lookup"><span data-stu-id="3db2f-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db2f-127">-PassThru</span></span>
<span data-ttu-id="3db2f-128">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3db2f-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3db2f-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3db2f-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3db2f-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3db2f-130">-VaultName</span></span>
<span data-ttu-id="3db2f-131">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3db2f-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3db2f-132">-Confirm</span></span>
<span data-ttu-id="3db2f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3db2f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db2f-134">-WhatIf</span></span>
<span data-ttu-id="3db2f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3db2f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db2f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3db2f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db2f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db2f-137">CommonParameters</span></span>
<span data-ttu-id="3db2f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3db2f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db2f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db2f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db2f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3db2f-140">INPUTS</span></span>

### <span data-ttu-id="3db2f-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3db2f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="3db2f-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3db2f-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="3db2f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3db2f-143">OUTPUTS</span></span>

### <span data-ttu-id="3db2f-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3db2f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3db2f-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="3db2f-145">NOTES</span></span>

## <span data-ttu-id="3db2f-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3db2f-146">RELATED LINKS</span></span>

[<span data-ttu-id="3db2f-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3db2f-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3db2f-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3db2f-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

