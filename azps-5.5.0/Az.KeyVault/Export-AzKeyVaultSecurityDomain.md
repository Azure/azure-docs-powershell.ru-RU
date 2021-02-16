---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237580"
---
# <span data-ttu-id="d4801-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="d4801-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="d4801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4801-102">SYNOPSIS</span></span>
<span data-ttu-id="d4801-103">Экспортируются данные домена безопасности управляемой службы HSM.</span><span class="sxs-lookup"><span data-stu-id="d4801-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="d4801-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4801-104">SYNTAX</span></span>

### <span data-ttu-id="d4801-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4801-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4801-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d4801-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4801-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4801-107">DESCRIPTION</span></span>
<span data-ttu-id="d4801-108">Экспорт данных домена безопасности управляемой службы HSM для импорта в другой HSM.</span><span class="sxs-lookup"><span data-stu-id="d4801-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="d4801-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4801-109">EXAMPLES</span></span>

### <span data-ttu-id="d4801-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4801-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="d4801-111">Эта команда извлекает управляемый HSM-файл testmhsm и сохраняет его резервную копию этого домена безопасности HSM в указанный выходной файл.</span><span class="sxs-lookup"><span data-stu-id="d4801-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="d4801-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4801-112">PARAMETERS</span></span>

### <span data-ttu-id="d4801-113">-Сертификаты</span><span class="sxs-lookup"><span data-stu-id="d4801-113">-Certificates</span></span>
<span data-ttu-id="d4801-114">Пути к сертификатам, которые используются для шифрования данных домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="d4801-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4801-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4801-115">-DefaultProfile</span></span>
<span data-ttu-id="d4801-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4801-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4801-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d4801-117">-Force</span></span>
<span data-ttu-id="d4801-118">Укажите, следует ли переописывать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="d4801-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="d4801-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4801-119">-InputObject</span></span>
<span data-ttu-id="d4801-120">Объект, представляющий управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="d4801-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="d4801-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4801-121">-Name</span></span>
<span data-ttu-id="d4801-122">Имя управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="d4801-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="d4801-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="d4801-123">-OutputPath</span></span>
<span data-ttu-id="d4801-124">Укажите путь, в который будут загружаться данные домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="d4801-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4801-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4801-125">-PassThru</span></span>
<span data-ttu-id="d4801-126">Если задан этот код, для успешного cmdlet возвращается boolean.</span><span class="sxs-lookup"><span data-stu-id="d4801-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="d4801-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="d4801-127">-Quorum</span></span>
<span data-ttu-id="d4801-128">Минимальное количество акций, необходимое для расшифровки домена безопасности для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4801-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4801-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4801-129">-Confirm</span></span>
<span data-ttu-id="d4801-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d4801-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4801-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4801-131">-WhatIf</span></span>
<span data-ttu-id="d4801-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4801-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4801-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4801-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4801-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4801-134">CommonParameters</span></span>
<span data-ttu-id="d4801-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4801-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4801-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4801-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4801-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4801-137">INPUTS</span></span>

### <span data-ttu-id="d4801-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d4801-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="d4801-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4801-139">OUTPUTS</span></span>

### <span data-ttu-id="d4801-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4801-140">System.Boolean</span></span>

## <span data-ttu-id="d4801-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4801-141">NOTES</span></span>

## <span data-ttu-id="d4801-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4801-142">RELATED LINKS</span></span>
