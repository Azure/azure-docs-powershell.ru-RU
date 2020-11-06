---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c91aa7e43a36e1218f304c3675f1d3c9635002c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567985"
---
# <span data-ttu-id="8cbaf-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8cbaf-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8cbaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbaf-103">Удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cbaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cbaf-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cbaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cbaf-105">DESCRIPTION</span></span>
<span data-ttu-id="8cbaf-106">Командлет **Remove-AzureKeyVaultCertificateContact** удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="8cbaf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cbaf-107">EXAMPLES</span></span>

### <span data-ttu-id="8cbaf-108">Пример 1: Удаление контакта сертификата</span><span class="sxs-lookup"><span data-stu-id="8cbaf-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="8cbaf-109">Эта команда удаляет Patti Белова в качестве контакта сертификата для хранилища ключей Contoso01.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="8cbaf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cbaf-110">PARAMETERS</span></span>

### <span data-ttu-id="8cbaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbaf-111">-DefaultProfile</span></span>
<span data-ttu-id="8cbaf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8cbaf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cbaf-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8cbaf-113">-EmailAddress</span></span>
<span data-ttu-id="8cbaf-114">Указывает адрес электронной почты контакта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbaf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cbaf-115">-PassThru</span></span>
<span data-ttu-id="8cbaf-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8cbaf-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cbaf-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8cbaf-118">-VaultName</span></span>
<span data-ttu-id="8cbaf-119">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="8cbaf-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cbaf-120">-Confirm</span></span>
<span data-ttu-id="8cbaf-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbaf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbaf-122">-WhatIf</span></span>
<span data-ttu-id="8cbaf-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cbaf-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbaf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbaf-125">CommonParameters</span></span>
<span data-ttu-id="8cbaf-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbaf-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbaf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbaf-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cbaf-128">INPUTS</span></span>

### <span data-ttu-id="8cbaf-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="8cbaf-129">None</span></span>
<span data-ttu-id="8cbaf-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8cbaf-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cbaf-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cbaf-131">OUTPUTS</span></span>

### <span data-ttu-id="8cbaf-132">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSKeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="8cbaf-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact]</span></span>

## <span data-ttu-id="8cbaf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cbaf-133">NOTES</span></span>

## <span data-ttu-id="8cbaf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cbaf-134">RELATED LINKS</span></span>

[<span data-ttu-id="8cbaf-135">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8cbaf-135">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="8cbaf-136">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8cbaf-136">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

