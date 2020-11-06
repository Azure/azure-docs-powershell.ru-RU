---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c56dad380d1e5a43b3f4dafdc0e0e964e6264ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568910"
---
# <span data-ttu-id="cb049-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cb049-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cb049-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb049-102">SYNOPSIS</span></span>
<span data-ttu-id="cb049-103">Добавляет контакт для уведомлений сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb049-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb049-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb049-104">SYNTAX</span></span>

### <span data-ttu-id="cb049-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb049-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb049-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cb049-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb049-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb049-107">ByResourceId</span></span>
```
Add-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb049-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb049-108">DESCRIPTION</span></span>
<span data-ttu-id="cb049-109">Командлет **Add-AzureKeyVaultCertificateContact** добавляет контакт для хранилища ключей для уведомлений сертификата в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="cb049-109">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="cb049-110">Контакт получит обновления о таких событиях, как срок действия сертификата, например "закрыто", "сертификат обновлен" и т. д.</span><span class="sxs-lookup"><span data-stu-id="cb049-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="cb049-111">Эти события определяются политикой сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb049-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="cb049-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb049-112">EXAMPLES</span></span>

### <span data-ttu-id="cb049-113">Пример 1: Добавление контакта сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="cb049-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="cb049-114">Эта команда добавляет Patti Белова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает список контактов для хранилища "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="cb049-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="cb049-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb049-115">PARAMETERS</span></span>

### <span data-ttu-id="cb049-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb049-116">-DefaultProfile</span></span>
<span data-ttu-id="cb049-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cb049-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb049-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cb049-118">-EmailAddress</span></span>
<span data-ttu-id="cb049-119">Указывает адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="cb049-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb049-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb049-120">-InputObject</span></span>
<span data-ttu-id="cb049-121">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb049-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb049-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb049-122">-PassThru</span></span>
<span data-ttu-id="cb049-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="cb049-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb049-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb049-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb049-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb049-125">-ResourceId</span></span>
<span data-ttu-id="cb049-126">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cb049-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="cb049-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cb049-127">-VaultName</span></span>
<span data-ttu-id="cb049-128">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="cb049-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb049-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb049-129">-Confirm</span></span>
<span data-ttu-id="cb049-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb049-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb049-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb049-131">-WhatIf</span></span>
<span data-ttu-id="cb049-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb049-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb049-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb049-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb049-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb049-134">CommonParameters</span></span>
<span data-ttu-id="cb049-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb049-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb049-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb049-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb049-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb049-137">INPUTS</span></span>

### <span data-ttu-id="cb049-138">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cb049-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="cb049-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb049-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="cb049-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cb049-140">System.String</span></span>

## <span data-ttu-id="cb049-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb049-141">OUTPUTS</span></span>

### <span data-ttu-id="cb049-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cb049-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cb049-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb049-143">NOTES</span></span>

## <span data-ttu-id="cb049-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb049-144">RELATED LINKS</span></span>

[<span data-ttu-id="cb049-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cb049-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="cb049-146">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cb049-146">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

