---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249052"
---
# <span data-ttu-id="29d4e-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d4e-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="29d4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="29d4e-103">Удаление поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="29d4e-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="29d4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29d4e-104">SYNTAX</span></span>

### <span data-ttu-id="29d4e-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29d4e-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29d4e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="29d4e-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d4e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29d4e-107">DESCRIPTION</span></span>
<span data-ttu-id="29d4e-108">Командлет **Remove-AzKeyVaultCertificateIssuer** Удаляет поставщика сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="29d4e-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="29d4e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="29d4e-110">Пример 1: Удаление поставщика сертификата</span><span class="sxs-lookup"><span data-stu-id="29d4e-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="29d4e-111">Эта команда удаляет издателя сертификата с именем TestIssuer01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="29d4e-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="29d4e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29d4e-112">PARAMETERS</span></span>

### <span data-ttu-id="29d4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d4e-113">-DefaultProfile</span></span>
<span data-ttu-id="29d4e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="29d4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d4e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="29d4e-115">-Force</span></span>
<span data-ttu-id="29d4e-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="29d4e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29d4e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29d4e-117">-InputObject</span></span>
<span data-ttu-id="29d4e-118">Объект Issuer сертификата</span><span class="sxs-lookup"><span data-stu-id="29d4e-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="29d4e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29d4e-119">-Name</span></span>
<span data-ttu-id="29d4e-120">Указывает имя поставщика для удаления.</span><span class="sxs-lookup"><span data-stu-id="29d4e-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="29d4e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29d4e-121">-PassThru</span></span>
<span data-ttu-id="29d4e-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="29d4e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29d4e-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="29d4e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29d4e-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29d4e-124">-VaultName</span></span>
<span data-ttu-id="29d4e-125">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="29d4e-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="29d4e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29d4e-126">-Confirm</span></span>
<span data-ttu-id="29d4e-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29d4e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d4e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d4e-128">-WhatIf</span></span>
<span data-ttu-id="29d4e-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29d4e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d4e-130">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29d4e-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d4e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29d4e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d4e-132">CommonParameters</span></span>
<span data-ttu-id="29d4e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29d4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d4e-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29d4e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d4e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29d4e-135">INPUTS</span></span>

### <span data-ttu-id="29d4e-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="29d4e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="29d4e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29d4e-137">OUTPUTS</span></span>

### <span data-ttu-id="29d4e-138">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d4e-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="29d4e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="29d4e-139">NOTES</span></span>

## <span data-ttu-id="29d4e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29d4e-140">RELATED LINKS</span></span>

[<span data-ttu-id="29d4e-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d4e-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="29d4e-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29d4e-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


