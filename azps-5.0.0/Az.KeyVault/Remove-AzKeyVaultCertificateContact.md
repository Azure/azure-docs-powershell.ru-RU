---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249054"
---
# <span data-ttu-id="779f8-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="779f8-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="779f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="779f8-102">SYNOPSIS</span></span>
<span data-ttu-id="779f8-103">Удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="779f8-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="779f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="779f8-104">SYNTAX</span></span>

### <span data-ttu-id="779f8-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="779f8-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779f8-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="779f8-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779f8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="779f8-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="779f8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="779f8-108">DESCRIPTION</span></span>
<span data-ttu-id="779f8-109">Командлет **Remove-AzKeyVaultCertificateContact** удаляет контакт, зарегистрированный для уведомлений о сертификате из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="779f8-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="779f8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="779f8-110">EXAMPLES</span></span>

### <span data-ttu-id="779f8-111">Пример 1: Удаление контакта сертификата</span><span class="sxs-lookup"><span data-stu-id="779f8-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="779f8-112">Эта команда удаляет Patti Белова в качестве контакта сертификата для хранилища ключей Contoso01.</span><span class="sxs-lookup"><span data-stu-id="779f8-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="779f8-113">Если указана функция PassThru, командлет возвращает список остальных контактов сертификата.</span><span class="sxs-lookup"><span data-stu-id="779f8-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="779f8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="779f8-114">PARAMETERS</span></span>

### <span data-ttu-id="779f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779f8-115">-DefaultProfile</span></span>
<span data-ttu-id="779f8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="779f8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="779f8-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="779f8-117">-EmailAddress</span></span>
<span data-ttu-id="779f8-118">Указывает адрес электронной почты контакта, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="779f8-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="779f8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="779f8-119">-InputObject</span></span>
<span data-ttu-id="779f8-120">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="779f8-120">KeyVault object.</span></span>

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

### <span data-ttu-id="779f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="779f8-121">-PassThru</span></span>
<span data-ttu-id="779f8-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="779f8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="779f8-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="779f8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="779f8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="779f8-124">-ResourceId</span></span>
<span data-ttu-id="779f8-125">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="779f8-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="779f8-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="779f8-126">-VaultName</span></span>
<span data-ttu-id="779f8-127">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="779f8-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="779f8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="779f8-128">-Confirm</span></span>
<span data-ttu-id="779f8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="779f8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="779f8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="779f8-130">-WhatIf</span></span>
<span data-ttu-id="779f8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="779f8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="779f8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="779f8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="779f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779f8-133">CommonParameters</span></span>
<span data-ttu-id="779f8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="779f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779f8-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="779f8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779f8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="779f8-136">INPUTS</span></span>

### <span data-ttu-id="779f8-137">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="779f8-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="779f8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="779f8-138">System.String</span></span>

## <span data-ttu-id="779f8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="779f8-139">OUTPUTS</span></span>

### <span data-ttu-id="779f8-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="779f8-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="779f8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="779f8-141">NOTES</span></span>

## <span data-ttu-id="779f8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="779f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="779f8-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="779f8-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="779f8-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="779f8-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

