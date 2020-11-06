---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 69619b9f5ddd54e0d307a096cc967c307d1f36d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560152"
---
# <span data-ttu-id="10039-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10039-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="10039-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10039-102">SYNOPSIS</span></span>
<span data-ttu-id="10039-103">Задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="10039-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10039-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10039-104">SYNTAX</span></span>

### <span data-ttu-id="10039-105">Развернуто (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10039-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10039-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="10039-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10039-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10039-107">DESCRIPTION</span></span>
<span data-ttu-id="10039-108">Командлет Set-AzureKeyVaultCertificateIssuer задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="10039-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="10039-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10039-109">EXAMPLES</span></span>

### <span data-ttu-id="10039-110">Пример 1: Настройка поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="10039-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="10039-111">Эта команда задает свойства для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="10039-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="10039-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10039-112">PARAMETERS</span></span>

### <span data-ttu-id="10039-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="10039-113">-AccountId</span></span>
<span data-ttu-id="10039-114">Указывает идентификатор учетной записи для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="10039-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="10039-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="10039-115">-ApiKey</span></span>
<span data-ttu-id="10039-116">Указывает ключ API для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="10039-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="10039-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10039-117">-DefaultProfile</span></span>
<span data-ttu-id="10039-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10039-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10039-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10039-119">-InputObject</span></span>
<span data-ttu-id="10039-120">Указывает издателя сертификата, который нужно задать.</span><span class="sxs-lookup"><span data-stu-id="10039-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="10039-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="10039-121">-IssuerProvider</span></span>
<span data-ttu-id="10039-122">Указывает тип заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="10039-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="10039-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10039-123">-Name</span></span>
<span data-ttu-id="10039-124">Указывает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="10039-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="10039-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="10039-125">-OrganizationDetails</span></span>
<span data-ttu-id="10039-126">Сведения об организации, которые будут использоваться для поставщика.</span><span class="sxs-lookup"><span data-stu-id="10039-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="10039-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10039-127">-PassThru</span></span>
<span data-ttu-id="10039-128">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="10039-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="10039-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="10039-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="10039-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="10039-130">-VaultName</span></span>
<span data-ttu-id="10039-131">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="10039-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="10039-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10039-132">-Confirm</span></span>
<span data-ttu-id="10039-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10039-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10039-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10039-134">-WhatIf</span></span>
<span data-ttu-id="10039-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10039-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10039-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10039-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10039-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10039-137">CommonParameters</span></span>
<span data-ttu-id="10039-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10039-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10039-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10039-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10039-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10039-140">INPUTS</span></span>

### <span data-ttu-id="10039-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="10039-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>
<span data-ttu-id="10039-142">Параметры: OrganizationDetails (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10039-142">Parameters: OrganizationDetails (ByValue)</span></span>

### <span data-ttu-id="10039-143">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="10039-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="10039-144">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10039-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="10039-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10039-145">OUTPUTS</span></span>

### <span data-ttu-id="10039-146">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10039-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="10039-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="10039-147">NOTES</span></span>

## <span data-ttu-id="10039-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10039-148">RELATED LINKS</span></span>

[<span data-ttu-id="10039-149">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10039-149">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="10039-150">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="10039-150">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

