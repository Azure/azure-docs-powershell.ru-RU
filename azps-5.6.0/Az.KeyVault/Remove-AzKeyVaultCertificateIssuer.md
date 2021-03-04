---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3a85b92b930ef24e4cb613de28f6a66b530222cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952584"
---
# <span data-ttu-id="f85ed-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f85ed-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f85ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f85ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f85ed-103">Удаляет выпускаемого сертификата из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f85ed-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f85ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f85ed-104">SYNTAX</span></span>

### <span data-ttu-id="f85ed-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f85ed-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f85ed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f85ed-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f85ed-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f85ed-107">DESCRIPTION</span></span>
<span data-ttu-id="f85ed-108">Cmdlet **Remove-AzKeyVaultCertificateIssuer** удаляет проблему с сертификатом из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f85ed-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="f85ed-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f85ed-109">EXAMPLES</span></span>

### <span data-ttu-id="f85ed-110">Пример 1. Удаление выпуска сертификата</span><span class="sxs-lookup"><span data-stu-id="f85ed-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="f85ed-111">Эта команда удаляет выпускаемого сертификата TestIssuer01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f85ed-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f85ed-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f85ed-112">PARAMETERS</span></span>

### <span data-ttu-id="f85ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85ed-113">-DefaultProfile</span></span>
<span data-ttu-id="f85ed-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f85ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f85ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f85ed-115">-Force</span></span>
<span data-ttu-id="f85ed-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f85ed-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f85ed-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f85ed-117">-InputObject</span></span>
<span data-ttu-id="f85ed-118">Объект-эмитент сертификата</span><span class="sxs-lookup"><span data-stu-id="f85ed-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="f85ed-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f85ed-119">-Name</span></span>
<span data-ttu-id="f85ed-120">Указывает имя удаляемого выпуска.</span><span class="sxs-lookup"><span data-stu-id="f85ed-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="f85ed-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f85ed-121">-PassThru</span></span>
<span data-ttu-id="f85ed-122">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f85ed-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f85ed-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f85ed-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f85ed-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f85ed-124">-VaultName</span></span>
<span data-ttu-id="f85ed-125">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="f85ed-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f85ed-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f85ed-126">-Confirm</span></span>
<span data-ttu-id="f85ed-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f85ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f85ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f85ed-128">-WhatIf</span></span>
<span data-ttu-id="f85ed-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f85ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f85ed-130">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f85ed-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f85ed-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f85ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f85ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85ed-132">CommonParameters</span></span>
<span data-ttu-id="f85ed-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85ed-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f85ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85ed-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f85ed-135">INPUTS</span></span>

### <span data-ttu-id="f85ed-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f85ed-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="f85ed-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f85ed-137">OUTPUTS</span></span>

### <span data-ttu-id="f85ed-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f85ed-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f85ed-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f85ed-139">NOTES</span></span>

## <span data-ttu-id="f85ed-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f85ed-140">RELATED LINKS</span></span>

[<span data-ttu-id="f85ed-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f85ed-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f85ed-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f85ed-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


