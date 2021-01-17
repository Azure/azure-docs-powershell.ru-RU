---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323879"
---
# <span data-ttu-id="e9755-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e9755-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e9755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9755-102">SYNOPSIS</span></span>
<span data-ttu-id="e9755-103">Удаляет контакт, зарегистрированный для уведомлений о сертификате, из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e9755-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="e9755-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9755-104">SYNTAX</span></span>

### <span data-ttu-id="e9755-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9755-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9755-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e9755-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9755-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9755-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9755-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9755-108">DESCRIPTION</span></span>
<span data-ttu-id="e9755-109">**Cmdlet Remove-AzKeyVaultCertificateContact** удаляет контакт, зарегистрированный для уведомлений о сертификате, из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e9755-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="e9755-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9755-110">EXAMPLES</span></span>

### <span data-ttu-id="e9755-111">Пример 1. Удаление контакта сертификата</span><span class="sxs-lookup"><span data-stu-id="e9755-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="e9755-112">Эта команда удаляет Комси Полномер как контакт сертификата для хранилища ключей Contoso01.</span><span class="sxs-lookup"><span data-stu-id="e9755-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="e9755-113">Если задан passThru, cmdlet возвращает список оставшихся контактов сертификата.</span><span class="sxs-lookup"><span data-stu-id="e9755-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="e9755-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9755-114">PARAMETERS</span></span>

### <span data-ttu-id="e9755-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9755-115">-DefaultProfile</span></span>
<span data-ttu-id="e9755-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e9755-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9755-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e9755-117">-EmailAddress</span></span>
<span data-ttu-id="e9755-118">Определяет адрес электронной почты контакта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e9755-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="e9755-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9755-119">-InputObject</span></span>
<span data-ttu-id="e9755-120">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e9755-120">KeyVault object.</span></span>

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

### <span data-ttu-id="e9755-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9755-121">-PassThru</span></span>
<span data-ttu-id="e9755-122">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e9755-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e9755-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e9755-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9755-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9755-124">-ResourceId</span></span>
<span data-ttu-id="e9755-125">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e9755-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e9755-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e9755-126">-VaultName</span></span>
<span data-ttu-id="e9755-127">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="e9755-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9755-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9755-128">-Confirm</span></span>
<span data-ttu-id="e9755-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e9755-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9755-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9755-130">-WhatIf</span></span>
<span data-ttu-id="e9755-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9755-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9755-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9755-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9755-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9755-133">CommonParameters</span></span>
<span data-ttu-id="e9755-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9755-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9755-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9755-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9755-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9755-136">INPUTS</span></span>

### <span data-ttu-id="e9755-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e9755-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e9755-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e9755-138">System.String</span></span>

## <span data-ttu-id="e9755-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9755-139">OUTPUTS</span></span>

### <span data-ttu-id="e9755-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e9755-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e9755-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9755-141">NOTES</span></span>

## <span data-ttu-id="e9755-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9755-142">RELATED LINKS</span></span>

[<span data-ttu-id="e9755-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e9755-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e9755-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e9755-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

