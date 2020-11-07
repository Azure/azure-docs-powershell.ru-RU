---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910285"
---
# <span data-ttu-id="3a60b-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3a60b-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3a60b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a60b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a60b-103">Удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3a60b-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="3a60b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a60b-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a60b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a60b-105">DESCRIPTION</span></span>
<span data-ttu-id="3a60b-106">Командлет **Remove-AzKeyVaultCertificateContact** удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3a60b-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="3a60b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a60b-107">EXAMPLES</span></span>

### <span data-ttu-id="3a60b-108">Пример 1: Удаление контакта сертификата</span><span class="sxs-lookup"><span data-stu-id="3a60b-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="3a60b-109">Эта команда удаляет Patti Белова в качестве контакта сертификата для хранилища ключей Contoso01.</span><span class="sxs-lookup"><span data-stu-id="3a60b-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="3a60b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a60b-110">PARAMETERS</span></span>

### <span data-ttu-id="3a60b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a60b-111">-DefaultProfile</span></span>
<span data-ttu-id="3a60b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a60b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a60b-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3a60b-113">-EmailAddress</span></span>
<span data-ttu-id="3a60b-114">Указывает адрес электронной почты контакта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3a60b-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="3a60b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a60b-115">-PassThru</span></span>
<span data-ttu-id="3a60b-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3a60b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a60b-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3a60b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a60b-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3a60b-118">-VaultName</span></span>
<span data-ttu-id="3a60b-119">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3a60b-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="3a60b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a60b-120">-Confirm</span></span>
<span data-ttu-id="3a60b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a60b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a60b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a60b-122">-WhatIf</span></span>
<span data-ttu-id="3a60b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a60b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a60b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a60b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a60b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a60b-125">CommonParameters</span></span>
<span data-ttu-id="3a60b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a60b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a60b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a60b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a60b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a60b-128">INPUTS</span></span>

### <span data-ttu-id="3a60b-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="3a60b-129">None</span></span>
<span data-ttu-id="3a60b-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3a60b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a60b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a60b-131">OUTPUTS</span></span>

### <span data-ttu-id="3a60b-132">System. Collections. Generic. List ' 1 [Microsoft. Azure. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="3a60b-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="3a60b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a60b-133">NOTES</span></span>

## <span data-ttu-id="3a60b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a60b-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a60b-135">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3a60b-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="3a60b-136">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3a60b-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

