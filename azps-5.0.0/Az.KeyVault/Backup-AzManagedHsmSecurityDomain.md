---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312374"
---
# <span data-ttu-id="dfdb3-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="dfdb3-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="dfdb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="dfdb3-103">Резервное копирование данных домена безопасности управляемого HSM-файла для восстановления.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="dfdb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfdb3-104">SYNTAX</span></span>

### <span data-ttu-id="dfdb3-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfdb3-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfdb3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dfdb3-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfdb3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfdb3-107">DESCRIPTION</span></span>
<span data-ttu-id="dfdb3-108">Этот командлет производит резервное копирование данных домена безопасности управляемого HSM-файла для восстановления.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="dfdb3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfdb3-109">EXAMPLES</span></span>

### <span data-ttu-id="dfdb3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dfdb3-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="dfdb3-111">Эта команда извлекает управляемый HSM-файл с именем testmhsm и сохраняет резервную копию этого управляемого домена безопасности HSM в указанном выходном файле.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="dfdb3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfdb3-112">PARAMETERS</span></span>

### <span data-ttu-id="dfdb3-113">-Сертификаты</span><span class="sxs-lookup"><span data-stu-id="dfdb3-113">-Certificates</span></span>
<span data-ttu-id="dfdb3-114">Пути к сертификатам, которые используются для шифрования данных домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="dfdb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfdb3-115">-DefaultProfile</span></span>
<span data-ttu-id="dfdb3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfdb3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dfdb3-117">-Force</span></span>
<span data-ttu-id="dfdb3-118">Укажите, следует ли перезаписать существующий файл.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="dfdb3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfdb3-119">-InputObject</span></span>
<span data-ttu-id="dfdb3-120">Объект, представляющий управляемый HSM-аппарат.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="dfdb3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dfdb3-121">-Name</span></span>
<span data-ttu-id="dfdb3-122">Имя управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="dfdb3-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="dfdb3-123">-OutputPath</span></span>
<span data-ttu-id="dfdb3-124">Укажите путь к папке, в которую будут скачаны данные домена безопасности.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="dfdb3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfdb3-125">-PassThru</span></span>
<span data-ttu-id="dfdb3-126">Если задано значение, при успешном завершении командлета будет возвращаться логическая переменная.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="dfdb3-127">-Кворум</span><span class="sxs-lookup"><span data-stu-id="dfdb3-127">-Quorum</span></span>
<span data-ttu-id="dfdb3-128">Минимальное количество общих ресурсов, необходимых для расшифровки домена безопасности для восстановления.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="dfdb3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfdb3-129">-Confirm</span></span>
<span data-ttu-id="dfdb3-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfdb3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfdb3-131">-WhatIf</span></span>
<span data-ttu-id="dfdb3-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfdb3-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfdb3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfdb3-134">CommonParameters</span></span>
<span data-ttu-id="dfdb3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfdb3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfdb3-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfdb3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfdb3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfdb3-137">INPUTS</span></span>

### <span data-ttu-id="dfdb3-138">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="dfdb3-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="dfdb3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfdb3-139">OUTPUTS</span></span>

### <span data-ttu-id="dfdb3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfdb3-140">System.Boolean</span></span>

## <span data-ttu-id="dfdb3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfdb3-141">NOTES</span></span>

## <span data-ttu-id="dfdb3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfdb3-142">RELATED LINKS</span></span>
