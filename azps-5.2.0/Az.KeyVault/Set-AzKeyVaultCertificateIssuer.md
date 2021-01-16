---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393879"
---
# <span data-ttu-id="9be69-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9be69-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9be69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9be69-102">SYNOPSIS</span></span>
<span data-ttu-id="9be69-103">Задает проблему с сертификатом в хранилище ключа.</span><span class="sxs-lookup"><span data-stu-id="9be69-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="9be69-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9be69-104">SYNTAX</span></span>

### <span data-ttu-id="9be69-105">Расширенное (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9be69-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9be69-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="9be69-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9be69-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9be69-107">DESCRIPTION</span></span>
<span data-ttu-id="9be69-108">Этот Set-AzKeyVaultCertificateIssuer задает проблему с сертификатом в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="9be69-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="9be69-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9be69-109">EXAMPLES</span></span>

### <span data-ttu-id="9be69-110">Пример 1. Настройка выпуска сертификата</span><span class="sxs-lookup"><span data-stu-id="9be69-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="9be69-111">Эта команда задает свойства для выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="9be69-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="9be69-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9be69-112">PARAMETERS</span></span>

### <span data-ttu-id="9be69-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="9be69-113">-AccountId</span></span>
<span data-ttu-id="9be69-114">Указывает ИД учетной записи для выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="9be69-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="9be69-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="9be69-115">-ApiKey</span></span>
<span data-ttu-id="9be69-116">Указывает ключ API для выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="9be69-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="9be69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be69-117">-DefaultProfile</span></span>
<span data-ttu-id="9be69-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9be69-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9be69-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9be69-119">-InputObject</span></span>
<span data-ttu-id="9be69-120">Указывает нужного выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="9be69-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="9be69-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="9be69-121">-IssuerProvider</span></span>
<span data-ttu-id="9be69-122">Определяет тип выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="9be69-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="9be69-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9be69-123">-Name</span></span>
<span data-ttu-id="9be69-124">Указывает имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="9be69-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="9be69-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="9be69-125">-OrganizationDetails</span></span>
<span data-ttu-id="9be69-126">Сведения об организации, которые будут использоваться с этим эмитентом.</span><span class="sxs-lookup"><span data-stu-id="9be69-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="9be69-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9be69-127">-PassThru</span></span>
<span data-ttu-id="9be69-128">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9be69-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9be69-129">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9be69-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9be69-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9be69-130">-VaultName</span></span>
<span data-ttu-id="9be69-131">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="9be69-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="9be69-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9be69-132">-Confirm</span></span>
<span data-ttu-id="9be69-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9be69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9be69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9be69-134">-WhatIf</span></span>
<span data-ttu-id="9be69-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9be69-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9be69-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9be69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9be69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be69-137">CommonParameters</span></span>
<span data-ttu-id="9be69-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be69-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9be69-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be69-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9be69-140">INPUTS</span></span>

### <span data-ttu-id="9be69-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="9be69-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="9be69-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9be69-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="9be69-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9be69-143">OUTPUTS</span></span>

### <span data-ttu-id="9be69-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9be69-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9be69-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9be69-145">NOTES</span></span>

## <span data-ttu-id="9be69-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9be69-146">RELATED LINKS</span></span>

[<span data-ttu-id="9be69-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9be69-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9be69-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9be69-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

