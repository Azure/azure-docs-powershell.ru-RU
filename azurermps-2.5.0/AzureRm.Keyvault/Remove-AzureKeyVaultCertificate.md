---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913347"
---
# <span data-ttu-id="fe4b1-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe4b1-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="fe4b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4b1-103">Удаляет сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe4b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe4b1-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe4b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe4b1-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4b1-106">Командлет **Remove-AzureKeyVaultCertificate** Удаляет сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="fe4b1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe4b1-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4b1-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="fe4b1-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="fe4b1-109">Эта команда удаляет сертификат с именем SelfSigned01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="fe4b1-110">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="fe4b1-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fe4b1-111">Таким образом, командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="fe4b1-112">Пример 3: Удаление удаленного сертификата из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="fe4b1-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="fe4b1-113">Эта команда окончательно удаляет сертификат с именем "MyCert" из хранилища ключей с именем "contoso".</span><span class="sxs-lookup"><span data-stu-id="fe4b1-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="fe4b1-114">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю в этом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="fe4b1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe4b1-115">PARAMETERS</span></span>

### <span data-ttu-id="fe4b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4b1-116">-DefaultProfile</span></span>
<span data-ttu-id="fe4b1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe4b1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe4b1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fe4b1-118">-Force</span></span>
<span data-ttu-id="fe4b1-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe4b1-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fe4b1-120">-InRemovedState</span></span>
<span data-ttu-id="fe4b1-121">Если он указан, окончательно удаляет ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="fe4b1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe4b1-122">-Name</span></span>
<span data-ttu-id="fe4b1-123">Указывает имя сертификата, который этот командлет удаляет из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="fe4b1-124">Этот командлет создает полное доменное имя (FQDN) сертификата на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4b1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe4b1-125">-PassThru</span></span>
<span data-ttu-id="fe4b1-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe4b1-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe4b1-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe4b1-128">-VaultName</span></span>
<span data-ttu-id="fe4b1-129">Указывает имя хранилища ключей, из которого этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="fe4b1-130">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="fe4b1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe4b1-131">-Confirm</span></span>
<span data-ttu-id="fe4b1-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe4b1-133">-WhatIf</span></span>
<span data-ttu-id="fe4b1-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe4b1-135">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe4b1-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4b1-137">CommonParameters</span></span>
<span data-ttu-id="fe4b1-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe4b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4b1-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4b1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4b1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe4b1-140">INPUTS</span></span>

## <span data-ttu-id="fe4b1-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe4b1-141">OUTPUTS</span></span>

### <span data-ttu-id="fe4b1-142">Microsoft. Azure. Commands. KeyVault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="fe4b1-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="fe4b1-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe4b1-143">NOTES</span></span>

## <span data-ttu-id="fe4b1-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe4b1-144">RELATED LINKS</span></span>

[<span data-ttu-id="fe4b1-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe4b1-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fe4b1-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe4b1-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fe4b1-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fe4b1-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fe4b1-148">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="fe4b1-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
