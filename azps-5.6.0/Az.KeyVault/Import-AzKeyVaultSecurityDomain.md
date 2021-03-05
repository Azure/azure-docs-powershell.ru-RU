---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 3175685478afada44e8870e772a56ce91992bbc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001400"
---
# <span data-ttu-id="1646f-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="1646f-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="1646f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1646f-102">SYNOPSIS</span></span>
<span data-ttu-id="1646f-103">Импортируются ранее экспортируемые данные домена безопасности в управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="1646f-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="1646f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1646f-104">SYNTAX</span></span>

### <span data-ttu-id="1646f-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1646f-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1646f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1646f-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1646f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1646f-107">DESCRIPTION</span></span>
<span data-ttu-id="1646f-108">Этот cmdlet импортирует ранее экспортируемые данные домена безопасности в управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="1646f-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="1646f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1646f-109">EXAMPLES</span></span>

### <span data-ttu-id="1646f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1646f-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="1646f-111">Во-первых, для расшифровки данных домена безопасности необходимы ключи.</span><span class="sxs-lookup"><span data-stu-id="1646f-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="1646f-112">Затем с помощью команды **Import-AzKeyVaultSecurityDomain** данные домена безопасности восстанавливаются в управляемой службе управления безопасностью с помощью этих ключей.</span><span class="sxs-lookup"><span data-stu-id="1646f-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="1646f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1646f-113">PARAMETERS</span></span>

### <span data-ttu-id="1646f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1646f-114">-DefaultProfile</span></span>
<span data-ttu-id="1646f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1646f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1646f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1646f-116">-InputObject</span></span>
<span data-ttu-id="1646f-117">Объект, представляющий управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="1646f-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="1646f-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="1646f-118">-Keys</span></span>
<span data-ttu-id="1646f-119">Сведения о ключах, используемых для расшифровки данных домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="1646f-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="1646f-120">Посмотрите примеры того, как она построена.</span><span class="sxs-lookup"><span data-stu-id="1646f-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="1646f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1646f-121">-Name</span></span>
<span data-ttu-id="1646f-122">Имя управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="1646f-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="1646f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1646f-123">-PassThru</span></span>
<span data-ttu-id="1646f-124">Если задан этот код, для успешного cmdlet возвращается boolean.</span><span class="sxs-lookup"><span data-stu-id="1646f-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="1646f-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="1646f-125">-SecurityDomainPath</span></span>
<span data-ttu-id="1646f-126">Укажите путь к зашифрованным данным домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="1646f-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="1646f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1646f-127">-Confirm</span></span>
<span data-ttu-id="1646f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1646f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1646f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1646f-129">-WhatIf</span></span>
<span data-ttu-id="1646f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1646f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1646f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1646f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1646f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1646f-132">CommonParameters</span></span>
<span data-ttu-id="1646f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1646f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1646f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1646f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1646f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1646f-135">INPUTS</span></span>

### <span data-ttu-id="1646f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1646f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="1646f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1646f-137">OUTPUTS</span></span>

### <span data-ttu-id="1646f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1646f-138">System.Boolean</span></span>

## <span data-ttu-id="1646f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1646f-139">NOTES</span></span>

## <span data-ttu-id="1646f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1646f-140">RELATED LINKS</span></span>
