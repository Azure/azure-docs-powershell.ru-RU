---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 430a909e76c08ba0c19c18072fdf019cd2fa7b29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914114"
---
# <span data-ttu-id="87bf2-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="87bf2-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="87bf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="87bf2-103">Задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="87bf2-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87bf2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87bf2-104">SYNTAX</span></span>

### <span data-ttu-id="87bf2-105">Развернуто (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87bf2-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87bf2-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="87bf2-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87bf2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87bf2-107">DESCRIPTION</span></span>
<span data-ttu-id="87bf2-108">Командлет Set-AzureKeyVaultCertificateIssuer задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="87bf2-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="87bf2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87bf2-109">EXAMPLES</span></span>

### <span data-ttu-id="87bf2-110">Пример 1: Настройка поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="87bf2-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="87bf2-111">Эта команда задает свойства для заверителя сертификата, а затем сохраняет его в переменной $Issuer.</span><span class="sxs-lookup"><span data-stu-id="87bf2-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="87bf2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87bf2-112">PARAMETERS</span></span>

### <span data-ttu-id="87bf2-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="87bf2-113">-AccountId</span></span>
<span data-ttu-id="87bf2-114">Указывает идентификатор учетной записи для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="87bf2-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="87bf2-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="87bf2-115">-ApiKey</span></span>
<span data-ttu-id="87bf2-116">Указывает ключ API для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="87bf2-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="87bf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bf2-117">-DefaultProfile</span></span>
<span data-ttu-id="87bf2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="87bf2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87bf2-119">-Issuer</span><span class="sxs-lookup"><span data-stu-id="87bf2-119">-Issuer</span></span>
<span data-ttu-id="87bf2-120">Указывает издателя сертификата, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="87bf2-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bf2-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="87bf2-121">-IssuerProvider</span></span>
<span data-ttu-id="87bf2-122">Указывает тип заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="87bf2-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="87bf2-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87bf2-123">-Name</span></span>
<span data-ttu-id="87bf2-124">Указывает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="87bf2-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="87bf2-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="87bf2-125">-OrganizationDetails</span></span>
<span data-ttu-id="87bf2-126">Сведения об организации, которые будут использоваться для поставщика.</span><span class="sxs-lookup"><span data-stu-id="87bf2-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87bf2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87bf2-127">-PassThru</span></span>
<span data-ttu-id="87bf2-128">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="87bf2-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="87bf2-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="87bf2-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="87bf2-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87bf2-130">-VaultName</span></span>
<span data-ttu-id="87bf2-131">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="87bf2-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="87bf2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87bf2-132">-Confirm</span></span>
<span data-ttu-id="87bf2-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87bf2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87bf2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87bf2-134">-WhatIf</span></span>
<span data-ttu-id="87bf2-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87bf2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87bf2-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87bf2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87bf2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bf2-137">CommonParameters</span></span>
<span data-ttu-id="87bf2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87bf2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bf2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87bf2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bf2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87bf2-140">INPUTS</span></span>

## <span data-ttu-id="87bf2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87bf2-141">OUTPUTS</span></span>

### <span data-ttu-id="87bf2-142">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="87bf2-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="87bf2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="87bf2-143">NOTES</span></span>

## <span data-ttu-id="87bf2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87bf2-144">RELATED LINKS</span></span>

[<span data-ttu-id="87bf2-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="87bf2-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="87bf2-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="87bf2-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

