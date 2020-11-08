---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250195"
---
# <span data-ttu-id="ca71b-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="ca71b-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="ca71b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca71b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca71b-103">Восстановление предыдущих резервных копий данных домена безопасности в управляемый HSM-объект.</span><span class="sxs-lookup"><span data-stu-id="ca71b-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="ca71b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca71b-104">SYNTAX</span></span>

### <span data-ttu-id="ca71b-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca71b-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca71b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca71b-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca71b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca71b-107">DESCRIPTION</span></span>
<span data-ttu-id="ca71b-108">Этот командлет восстанавливает предшествующие резервные копии данных домена безопасности в управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="ca71b-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="ca71b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca71b-109">EXAMPLES</span></span>

### <span data-ttu-id="ca71b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca71b-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="ca71b-111">Сначала для расшифровки данных домена безопасности необходимо предоставить ключи.</span><span class="sxs-lookup"><span data-stu-id="ca71b-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="ca71b-112">Затем команда **RESTORE-AzManagedHsmSecurityDomain** восстанавливает предшествующие резервные копии данных домена безопасности в управляемом HSM с помощью этих ключей.</span><span class="sxs-lookup"><span data-stu-id="ca71b-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="ca71b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca71b-113">PARAMETERS</span></span>

### <span data-ttu-id="ca71b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca71b-114">-DefaultProfile</span></span>
<span data-ttu-id="ca71b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca71b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca71b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca71b-116">-InputObject</span></span>
<span data-ttu-id="ca71b-117">Объект, представляющий управляемый HSM-аппарат.</span><span class="sxs-lookup"><span data-stu-id="ca71b-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca71b-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="ca71b-118">-Keys</span></span>
<span data-ttu-id="ca71b-119">Сведения о ключах, используемых для расшифровки данных домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="ca71b-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="ca71b-120">Посмотрите примеры того, как оно создано.</span><span class="sxs-lookup"><span data-stu-id="ca71b-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca71b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca71b-121">-Name</span></span>
<span data-ttu-id="ca71b-122">Имя управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="ca71b-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca71b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca71b-123">-PassThru</span></span>
<span data-ttu-id="ca71b-124">Если задано значение, при успешном завершении командлета будет возвращаться логическая переменная.</span><span class="sxs-lookup"><span data-stu-id="ca71b-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="ca71b-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="ca71b-125">-SecurityDomainPath</span></span>
<span data-ttu-id="ca71b-126">Укажите путь к зашифрованным данным домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="ca71b-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca71b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca71b-127">-Confirm</span></span>
<span data-ttu-id="ca71b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca71b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca71b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca71b-129">-WhatIf</span></span>
<span data-ttu-id="ca71b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca71b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca71b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca71b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca71b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca71b-132">CommonParameters</span></span>
<span data-ttu-id="ca71b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca71b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca71b-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca71b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca71b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca71b-135">INPUTS</span></span>

### <span data-ttu-id="ca71b-136">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ca71b-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="ca71b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca71b-137">OUTPUTS</span></span>

### <span data-ttu-id="ca71b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca71b-138">System.Boolean</span></span>

## <span data-ttu-id="ca71b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca71b-139">NOTES</span></span>

## <span data-ttu-id="ca71b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca71b-140">RELATED LINKS</span></span>
