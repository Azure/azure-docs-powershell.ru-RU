---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566711"
---
# <span data-ttu-id="49f68-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="49f68-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="49f68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49f68-102">SYNOPSIS</span></span>
<span data-ttu-id="49f68-103">Задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="49f68-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49f68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49f68-104">SYNTAX</span></span>

### <span data-ttu-id="49f68-105">Развернуто (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49f68-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f68-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="49f68-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f68-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f68-107">DESCRIPTION</span></span>
<span data-ttu-id="49f68-108">Командлет Set-AzureKeyVaultCertificateIssuer задает поставщика сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="49f68-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="49f68-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49f68-109">EXAMPLES</span></span>

### <span data-ttu-id="49f68-110">Пример 1: Настройка поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="49f68-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="49f68-111">Эта команда задает свойства для заверителя сертификата, а затем сохраняет его в переменной $Issuer.</span><span class="sxs-lookup"><span data-stu-id="49f68-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="49f68-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49f68-112">PARAMETERS</span></span>

### <span data-ttu-id="49f68-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="49f68-113">-AccountId</span></span>
<span data-ttu-id="49f68-114">Указывает идентификатор учетной записи для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="49f68-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="49f68-115">-ApiKey</span></span>
<span data-ttu-id="49f68-116">Указывает ключ API для заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="49f68-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-117">-Issuer</span><span class="sxs-lookup"><span data-stu-id="49f68-117">-Issuer</span></span>
<span data-ttu-id="49f68-118">Указывает издателя сертификата, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="49f68-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="49f68-119">-IssuerProvider</span></span>
<span data-ttu-id="49f68-120">Указывает тип заверителя сертификата.</span><span class="sxs-lookup"><span data-stu-id="49f68-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49f68-121">-Name</span></span>
<span data-ttu-id="49f68-122">Указывает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="49f68-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="49f68-123">-OrganizationDetails</span></span>
<span data-ttu-id="49f68-124">Сведения об организации, которые будут использоваться для поставщика.</span><span class="sxs-lookup"><span data-stu-id="49f68-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f68-125">-PassThru</span></span>
<span data-ttu-id="49f68-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="49f68-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49f68-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="49f68-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49f68-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="49f68-128">-VaultName</span></span>
<span data-ttu-id="49f68-129">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="49f68-129">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49f68-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49f68-130">-Confirm</span></span>
<span data-ttu-id="49f68-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49f68-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f68-132">-WhatIf</span></span>
<span data-ttu-id="49f68-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49f68-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f68-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49f68-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f68-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f68-135">-DefaultProfile</span></span>
<span data-ttu-id="49f68-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49f68-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49f68-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f68-137">CommonParameters</span></span>
<span data-ttu-id="49f68-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49f68-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f68-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f68-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f68-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49f68-140">INPUTS</span></span>

## <span data-ttu-id="49f68-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49f68-141">OUTPUTS</span></span>

### <span data-ttu-id="49f68-142">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="49f68-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="49f68-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="49f68-143">NOTES</span></span>

## <span data-ttu-id="49f68-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49f68-144">RELATED LINKS</span></span>

[<span data-ttu-id="49f68-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="49f68-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="49f68-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="49f68-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

