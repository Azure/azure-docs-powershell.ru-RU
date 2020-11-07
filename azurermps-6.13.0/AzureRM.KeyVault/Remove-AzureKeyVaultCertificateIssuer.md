---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732718"
---
# <span data-ttu-id="4d93d-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4d93d-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4d93d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d93d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d93d-103">Удаление поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="4d93d-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d93d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d93d-104">SYNTAX</span></span>

### <span data-ttu-id="4d93d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d93d-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d93d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4d93d-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d93d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d93d-107">DESCRIPTION</span></span>
<span data-ttu-id="4d93d-108">Командлет **Remove-AzureKeyVaultCertificateIssuer** Удаляет поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="4d93d-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="4d93d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d93d-109">EXAMPLES</span></span>

### <span data-ttu-id="4d93d-110">Пример 1: Удаление поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="4d93d-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="4d93d-111">Эта команда удаляет издателя сертификата с именем TestIssuer01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4d93d-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="4d93d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d93d-112">PARAMETERS</span></span>

### <span data-ttu-id="4d93d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d93d-113">-DefaultProfile</span></span>
<span data-ttu-id="4d93d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d93d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d93d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4d93d-115">-Force</span></span>
<span data-ttu-id="4d93d-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d93d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d93d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d93d-117">-InputObject</span></span>
<span data-ttu-id="4d93d-118">Объект Issuer сертификата</span><span class="sxs-lookup"><span data-stu-id="4d93d-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d93d-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d93d-119">-Name</span></span>
<span data-ttu-id="4d93d-120">Указывает имя поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="4d93d-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d93d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d93d-121">-PassThru</span></span>
<span data-ttu-id="4d93d-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4d93d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4d93d-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4d93d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d93d-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4d93d-124">-VaultName</span></span>
<span data-ttu-id="4d93d-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="4d93d-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d93d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d93d-126">-Confirm</span></span>
<span data-ttu-id="4d93d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d93d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d93d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d93d-128">-WhatIf</span></span>
<span data-ttu-id="4d93d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d93d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d93d-130">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d93d-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d93d-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d93d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d93d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d93d-132">CommonParameters</span></span>
<span data-ttu-id="4d93d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d93d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d93d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d93d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d93d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d93d-135">INPUTS</span></span>

### <span data-ttu-id="4d93d-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4d93d-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="4d93d-137">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d93d-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4d93d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d93d-138">OUTPUTS</span></span>

### <span data-ttu-id="4d93d-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4d93d-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4d93d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d93d-140">NOTES</span></span>

## <span data-ttu-id="4d93d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d93d-141">RELATED LINKS</span></span>

[<span data-ttu-id="4d93d-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4d93d-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="4d93d-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4d93d-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


