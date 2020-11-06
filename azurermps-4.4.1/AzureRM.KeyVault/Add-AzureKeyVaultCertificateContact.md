---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568763"
---
# <span data-ttu-id="1fff1-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1fff1-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="1fff1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fff1-102">SYNOPSIS</span></span>
<span data-ttu-id="1fff1-103">Добавляет контакт для уведомлений сертификата.</span><span class="sxs-lookup"><span data-stu-id="1fff1-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fff1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fff1-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fff1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fff1-105">DESCRIPTION</span></span>
<span data-ttu-id="1fff1-106">Командлет **Add-AzureKeyVaultCertificateContact** добавляет контакт для хранилища ключей для уведомлений сертификата в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1fff1-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="1fff1-107">Контакт получит обновления о таких событиях, как срок действия сертификата, например "закрыто", "сертификат обновлен" и т. д.</span><span class="sxs-lookup"><span data-stu-id="1fff1-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="1fff1-108">Эти события определяются политикой сертификата.</span><span class="sxs-lookup"><span data-stu-id="1fff1-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="1fff1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fff1-109">EXAMPLES</span></span>

### <span data-ttu-id="1fff1-110">Пример 1: Добавление контакта сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="1fff1-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="1fff1-111">Эта команда добавляет Patti Белова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает объект **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="1fff1-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="1fff1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fff1-112">PARAMETERS</span></span>

### <span data-ttu-id="1fff1-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1fff1-113">-EmailAddress</span></span>
<span data-ttu-id="1fff1-114">Указывает адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="1fff1-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fff1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fff1-115">-PassThru</span></span>
<span data-ttu-id="1fff1-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1fff1-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1fff1-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1fff1-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fff1-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1fff1-118">-VaultName</span></span>
<span data-ttu-id="1fff1-119">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1fff1-119">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="1fff1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fff1-120">-Confirm</span></span>
<span data-ttu-id="1fff1-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fff1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fff1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fff1-122">-WhatIf</span></span>
<span data-ttu-id="1fff1-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fff1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fff1-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fff1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fff1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fff1-125">-DefaultProfile</span></span>
<span data-ttu-id="1fff1-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fff1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fff1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fff1-127">CommonParameters</span></span>
<span data-ttu-id="1fff1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fff1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fff1-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fff1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fff1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fff1-130">INPUTS</span></span>

## <span data-ttu-id="1fff1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fff1-131">OUTPUTS</span></span>

### <span data-ttu-id="1fff1-132">List<Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="1fff1-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="1fff1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fff1-133">NOTES</span></span>

## <span data-ttu-id="1fff1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fff1-134">RELATED LINKS</span></span>

[<span data-ttu-id="1fff1-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1fff1-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="1fff1-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="1fff1-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

