---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569019"
---
# <span data-ttu-id="db26b-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="db26b-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="db26b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db26b-102">SYNOPSIS</span></span>
<span data-ttu-id="db26b-103">Задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="db26b-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db26b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db26b-104">SYNTAX</span></span>

### <span data-ttu-id="db26b-105">Развернуто (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db26b-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db26b-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="db26b-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db26b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db26b-107">DESCRIPTION</span></span>
<span data-ttu-id="db26b-108">Командлет Set-AzureKeyVaultCertificateIssuer задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="db26b-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="db26b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db26b-109">EXAMPLES</span></span>

### <span data-ttu-id="db26b-110">Пример 1: Настройка поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="db26b-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="db26b-111">Эта команда задает свойства для заверителя сертификата, а затем сохраняет его в переменной $Issuer.</span><span class="sxs-lookup"><span data-stu-id="db26b-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="db26b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db26b-112">PARAMETERS</span></span>

### <span data-ttu-id="db26b-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="db26b-113">-AccountId</span></span>
<span data-ttu-id="db26b-114">Указывает идентификатор учетной записи для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="db26b-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="db26b-115">-ApiKey</span></span>
<span data-ttu-id="db26b-116">Указывает ключ API для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="db26b-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db26b-117">-DefaultProfile</span></span>
<span data-ttu-id="db26b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db26b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db26b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db26b-119">-InputObject</span></span>
<span data-ttu-id="db26b-120">Указывает издателя сертификата, который нужно задать.</span><span class="sxs-lookup"><span data-stu-id="db26b-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="db26b-121">-IssuerProvider</span></span>
<span data-ttu-id="db26b-122">Указывает тип заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="db26b-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db26b-123">-Name</span></span>
<span data-ttu-id="db26b-124">Указывает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="db26b-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="db26b-125">-OrganizationDetails</span></span>
<span data-ttu-id="db26b-126">Сведения об организации, которые будут использоваться для поставщика.</span><span class="sxs-lookup"><span data-stu-id="db26b-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db26b-127">-PassThru</span></span>
<span data-ttu-id="db26b-128">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="db26b-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db26b-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="db26b-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db26b-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="db26b-130">-VaultName</span></span>
<span data-ttu-id="db26b-131">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="db26b-131">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db26b-132">-Confirm</span></span>
<span data-ttu-id="db26b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db26b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db26b-134">-WhatIf</span></span>
<span data-ttu-id="db26b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db26b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db26b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db26b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db26b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db26b-137">CommonParameters</span></span>
<span data-ttu-id="db26b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db26b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db26b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db26b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db26b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db26b-140">INPUTS</span></span>

### <span data-ttu-id="db26b-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="db26b-141">None</span></span>
<span data-ttu-id="db26b-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="db26b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db26b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db26b-143">OUTPUTS</span></span>

### <span data-ttu-id="db26b-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db26b-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="db26b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="db26b-145">NOTES</span></span>

## <span data-ttu-id="db26b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db26b-146">RELATED LINKS</span></span>

[<span data-ttu-id="db26b-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="db26b-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="db26b-148">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="db26b-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

