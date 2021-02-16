---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237628"
---
# <span data-ttu-id="d7831-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d7831-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d7831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7831-102">SYNOPSIS</span></span>
<span data-ttu-id="d7831-103">Добавляет контакт для уведомлений о сертификате.</span><span class="sxs-lookup"><span data-stu-id="d7831-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="d7831-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7831-104">SYNTAX</span></span>

### <span data-ttu-id="d7831-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7831-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7831-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="d7831-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7831-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7831-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7831-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7831-108">DESCRIPTION</span></span>
<span data-ttu-id="d7831-109">**Cmdlet Add-AzKeyVaultCertificateContact** добавляет контакт в хранилище ключа для уведомлений о сертификате в хранилище ключа Azure.</span><span class="sxs-lookup"><span data-stu-id="d7831-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="d7831-110">Контакт получает обновления о событиях, таких как сертификат, срок действия истекает, сертификат продлен и так далее.</span><span class="sxs-lookup"><span data-stu-id="d7831-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="d7831-111">Эти события определяются политикой сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d7831-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="d7831-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7831-112">EXAMPLES</span></span>

### <span data-ttu-id="d7831-113">Пример 1. Добавление контакта сертификата хранилища ключа</span><span class="sxs-lookup"><span data-stu-id="d7831-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="d7831-114">Эта команда добавляет Климова в качестве контакта сертификата для хранилища ключей ContosoKV01 и возвращает список контактов для хранилища ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="d7831-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="d7831-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7831-115">PARAMETERS</span></span>

### <span data-ttu-id="d7831-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7831-116">-DefaultProfile</span></span>
<span data-ttu-id="d7831-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d7831-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7831-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d7831-118">-EmailAddress</span></span>
<span data-ttu-id="d7831-119">Определяет адрес электронной почты контакта.</span><span class="sxs-lookup"><span data-stu-id="d7831-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="d7831-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7831-120">-InputObject</span></span>
<span data-ttu-id="d7831-121">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7831-121">KeyVault object.</span></span>

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

### <span data-ttu-id="d7831-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7831-122">-PassThru</span></span>
<span data-ttu-id="d7831-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d7831-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7831-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d7831-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7831-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7831-125">-ResourceId</span></span>
<span data-ttu-id="d7831-126">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7831-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="d7831-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d7831-127">-VaultName</span></span>
<span data-ttu-id="d7831-128">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="d7831-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="d7831-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7831-129">-Confirm</span></span>
<span data-ttu-id="d7831-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7831-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7831-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7831-131">-WhatIf</span></span>
<span data-ttu-id="d7831-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7831-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7831-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d7831-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7831-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7831-134">CommonParameters</span></span>
<span data-ttu-id="d7831-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7831-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7831-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7831-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7831-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7831-137">INPUTS</span></span>

### <span data-ttu-id="d7831-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7831-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d7831-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d7831-139">System.String</span></span>

## <span data-ttu-id="d7831-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7831-140">OUTPUTS</span></span>

### <span data-ttu-id="d7831-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d7831-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="d7831-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7831-142">NOTES</span></span>

## <span data-ttu-id="d7831-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7831-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7831-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d7831-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="d7831-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="d7831-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

