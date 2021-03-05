---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d9d77eaac735044091aacbce6f92ee51be1210ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004024"
---
# <span data-ttu-id="0763f-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0763f-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0763f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0763f-102">SYNOPSIS</span></span>
<span data-ttu-id="0763f-103">Получает проблему с выдачей сертификата для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="0763f-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="0763f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0763f-104">SYNTAX</span></span>

### <span data-ttu-id="0763f-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0763f-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0763f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0763f-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0763f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0763f-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0763f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0763f-108">DESCRIPTION</span></span>
<span data-ttu-id="0763f-109">Для указанного выпуска сертификата или всех его авторов в хранилище ключей Azure возвращается cmdlet **Get-AzKeyVaultCertificateIssuer.**</span><span class="sxs-lookup"><span data-stu-id="0763f-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0763f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0763f-110">EXAMPLES</span></span>

### <span data-ttu-id="0763f-111">Пример 1. Получить проблему с сертификатом</span><span class="sxs-lookup"><span data-stu-id="0763f-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="0763f-112">Эта команда получает имя выпуска сертификата TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="0763f-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="0763f-113">Пример 2. Проблемы с сертификатами списков с использованием фильтрации</span><span class="sxs-lookup"><span data-stu-id="0763f-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="0763f-114">Эта команда возвращает выдачу сертификатов, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="0763f-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="0763f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0763f-115">PARAMETERS</span></span>

### <span data-ttu-id="0763f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0763f-116">-DefaultProfile</span></span>
<span data-ttu-id="0763f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0763f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0763f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0763f-118">-InputObject</span></span>
<span data-ttu-id="0763f-119">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0763f-119">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0763f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0763f-120">-Name</span></span>
<span data-ttu-id="0763f-121">Указывает имя нужного выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="0763f-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0763f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0763f-122">-ResourceId</span></span>
<span data-ttu-id="0763f-123">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0763f-123">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0763f-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0763f-124">-VaultName</span></span>
<span data-ttu-id="0763f-125">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="0763f-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0763f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0763f-126">CommonParameters</span></span>
<span data-ttu-id="0763f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0763f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0763f-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0763f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0763f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0763f-129">INPUTS</span></span>

### <span data-ttu-id="0763f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0763f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0763f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0763f-131">System.String</span></span>

## <span data-ttu-id="0763f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0763f-132">OUTPUTS</span></span>

### <span data-ttu-id="0763f-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0763f-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="0763f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0763f-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0763f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0763f-135">NOTES</span></span>

## <span data-ttu-id="0763f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0763f-136">RELATED LINKS</span></span>

[<span data-ttu-id="0763f-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0763f-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="0763f-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0763f-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


