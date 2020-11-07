---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912350"
---
# <span data-ttu-id="8d869-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8d869-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8d869-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d869-102">SYNOPSIS</span></span>
<span data-ttu-id="8d869-103">Восстановление сертификата из файла резервной копии в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8d869-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="8d869-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d869-104">SYNTAX</span></span>

### <span data-ttu-id="8d869-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d869-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d869-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d869-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d869-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d869-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d869-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d869-108">DESCRIPTION</span></span>
<span data-ttu-id="8d869-109">Командлет **RESTORE-AzKeyVaultCertificate** создает сертификат в указанном хранилище ключей из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8d869-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="8d869-110">Этот сертификат является репликой резервного сертификата во входном файле и имеет то же имя, что и у исходного сертификата.</span><span class="sxs-lookup"><span data-stu-id="8d869-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="8d869-111">Если в хранилище ключей уже есть сертификат с тем же именем, этот командлет не будет работать вместо перезаписи исходного сертификата.</span><span class="sxs-lookup"><span data-stu-id="8d869-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="8d869-112">Если резервная копия имеет несколько версий сертификата, все версии будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="8d869-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="8d869-113">Хранилище ключей, в котором вы восстановите сертификат, может отличаться от того, в котором находится резервная копия сертификата.</span><span class="sxs-lookup"><span data-stu-id="8d869-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="8d869-114">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="8d869-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="8d869-115">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="8d869-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="8d869-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d869-116">EXAMPLES</span></span>

### <span data-ttu-id="8d869-117">Пример 1: восстановление резервной копии сертификата</span><span class="sxs-lookup"><span data-stu-id="8d869-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="8d869-118">Эта команда восстанавливает сертификат, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8d869-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="8d869-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d869-119">PARAMETERS</span></span>

### <span data-ttu-id="8d869-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d869-120">-DefaultProfile</span></span>
<span data-ttu-id="8d869-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d869-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d869-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8d869-122">-InputFile</span></span>
<span data-ttu-id="8d869-123">Входной файл.</span><span class="sxs-lookup"><span data-stu-id="8d869-123">Input file.</span></span>
<span data-ttu-id="8d869-124">Входной файл, содержащий заархивированный блоб</span><span class="sxs-lookup"><span data-stu-id="8d869-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d869-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d869-125">-InputObject</span></span>
<span data-ttu-id="8d869-126">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d869-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d869-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d869-127">-ResourceId</span></span>
<span data-ttu-id="8d869-128">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="8d869-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="8d869-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8d869-129">-VaultName</span></span>
<span data-ttu-id="8d869-130">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="8d869-130">Vault name.</span></span>
<span data-ttu-id="8d869-131">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="8d869-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d869-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d869-132">-Confirm</span></span>
<span data-ttu-id="8d869-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d869-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d869-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d869-134">-WhatIf</span></span>
<span data-ttu-id="8d869-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d869-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d869-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d869-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d869-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d869-137">CommonParameters</span></span>
<span data-ttu-id="8d869-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d869-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d869-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d869-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d869-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d869-140">INPUTS</span></span>

### <span data-ttu-id="8d869-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d869-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8d869-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8d869-142">System.String</span></span>

## <span data-ttu-id="8d869-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d869-143">OUTPUTS</span></span>

### <span data-ttu-id="8d869-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8d869-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="8d869-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d869-145">NOTES</span></span>

## <span data-ttu-id="8d869-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d869-146">RELATED LINKS</span></span>
