---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065620"
---
# <span data-ttu-id="48106-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="48106-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="48106-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48106-102">SYNOPSIS</span></span>
<span data-ttu-id="48106-103">Добавляет контакт для уведомлений сертификата.</span><span class="sxs-lookup"><span data-stu-id="48106-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="48106-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48106-104">SYNTAX</span></span>

### <span data-ttu-id="48106-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48106-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48106-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="48106-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48106-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="48106-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48106-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48106-108">DESCRIPTION</span></span>
<span data-ttu-id="48106-109">Командлет **Add-AzKeyVaultCertificateContact** добавляет контакт для хранилища ключей для уведомлений сертификата в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="48106-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="48106-110">Контакт получит обновления о таких событиях, как срок действия сертификата, например "закрыто", "сертификат обновлен" и т. д.</span><span class="sxs-lookup"><span data-stu-id="48106-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="48106-111">Эти события определяются политикой сертификата.</span><span class="sxs-lookup"><span data-stu-id="48106-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="48106-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48106-112">EXAMPLES</span></span>

### <span data-ttu-id="48106-113">Пример 1: Добавление контакта сертификата для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="48106-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="48106-114">Эта команда добавляет Patti Белова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает список контактов для хранилища "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="48106-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="48106-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48106-115">PARAMETERS</span></span>

### <span data-ttu-id="48106-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48106-116">-DefaultProfile</span></span>
<span data-ttu-id="48106-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="48106-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48106-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="48106-118">-EmailAddress</span></span>
<span data-ttu-id="48106-119">Указывает адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="48106-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="48106-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48106-120">-InputObject</span></span>
<span data-ttu-id="48106-121">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="48106-121">KeyVault object.</span></span>

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

### <span data-ttu-id="48106-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48106-122">-PassThru</span></span>
<span data-ttu-id="48106-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="48106-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="48106-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="48106-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48106-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48106-125">-ResourceId</span></span>
<span data-ttu-id="48106-126">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="48106-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="48106-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="48106-127">-VaultName</span></span>
<span data-ttu-id="48106-128">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="48106-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="48106-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48106-129">-Confirm</span></span>
<span data-ttu-id="48106-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48106-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48106-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48106-131">-WhatIf</span></span>
<span data-ttu-id="48106-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48106-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48106-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48106-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48106-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48106-134">CommonParameters</span></span>
<span data-ttu-id="48106-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48106-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48106-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48106-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48106-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48106-137">INPUTS</span></span>

### <span data-ttu-id="48106-138">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="48106-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="48106-139">System. String</span><span class="sxs-lookup"><span data-stu-id="48106-139">System.String</span></span>

## <span data-ttu-id="48106-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48106-140">OUTPUTS</span></span>

### <span data-ttu-id="48106-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="48106-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="48106-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="48106-142">NOTES</span></span>

## <span data-ttu-id="48106-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48106-143">RELATED LINKS</span></span>

[<span data-ttu-id="48106-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="48106-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="48106-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="48106-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

