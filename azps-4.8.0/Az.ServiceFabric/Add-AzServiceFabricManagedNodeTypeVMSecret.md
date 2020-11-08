---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078739"
---
# <span data-ttu-id="15de0-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="15de0-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="15de0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15de0-102">SYNOPSIS</span></span>
<span data-ttu-id="15de0-103">Добавьте секретный ключ сертификата в тип узла.</span><span class="sxs-lookup"><span data-stu-id="15de0-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="15de0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15de0-104">SYNTAX</span></span>

### <span data-ttu-id="15de0-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15de0-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15de0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="15de0-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15de0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15de0-107">DESCRIPTION</span></span>
<span data-ttu-id="15de0-108">Добавьте секретный ключ сертификата в тип узла.</span><span class="sxs-lookup"><span data-stu-id="15de0-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="15de0-109">Секрет должен храниться в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="15de0-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="15de0-110">Дополнительные сведения о хранилище ключей можно найти в разделе что такое Azure Key Vault?</span><span class="sxs-lookup"><span data-stu-id="15de0-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="15de0-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="15de0-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="15de0-112">Дополнительные сведения о командлетах можно найти в статьях командлетов Azure Key Vault ( https://msdn.microsoft.com/library/azure/dn868052.aspx) в сетевой библиотеке разработчиков Microsoft Developer или в командлете Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="15de0-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="15de0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15de0-113">EXAMPLES</span></span>

### <span data-ttu-id="15de0-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15de0-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="15de0-115">Этот запятыми добавляет секрет сертификата из указанных keyvault и секретного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="15de0-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="15de0-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15de0-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="15de0-117">Этот запятыми добавляет секрет сертификата из указанного идентификатора keyvault и секрета с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="15de0-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="15de0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15de0-118">PARAMETERS</span></span>

### <span data-ttu-id="15de0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15de0-119">-AsJob</span></span>
<span data-ttu-id="15de0-120">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="15de0-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="15de0-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="15de0-121">-CertificateStore</span></span>
<span data-ttu-id="15de0-122">Определяет хранилище сертификатов на виртуальной машине, на которую нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="15de0-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="15de0-123">Указанное хранилище сертификатов является неявным в учетной записи LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="15de0-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="15de0-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="15de0-124">-CertificateUrl</span></span>
<span data-ttu-id="15de0-125">Это URL-адрес сертификата, который был передан в хранилище ключей в качестве секрета.</span><span class="sxs-lookup"><span data-stu-id="15de0-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="15de0-126">Дополнительные сведения о добавлении секрета в хранилище ключей можно найти в разделе \[ Добавление ключа или секрета в хранилище ключей \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="15de0-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="15de0-127">В этом случае необходимо, чтобы ваш сертификат имел кодировку Base64 для следующего объекта JSON, который кодируется в UTF-8: \<br\> \<br\> { \<br\> "Data": " \<Base64-encoded-certificate\> ", "," пароль ":" \<br\> PFX ", \<br\> " Password ":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="15de0-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="15de0-128">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="15de0-128">-ClusterName</span></span>
<span data-ttu-id="15de0-129">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="15de0-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15de0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15de0-130">-DefaultProfile</span></span>
<span data-ttu-id="15de0-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15de0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15de0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15de0-132">-InputObject</span></span>
<span data-ttu-id="15de0-133">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="15de0-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15de0-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15de0-134">-Name</span></span>
<span data-ttu-id="15de0-135">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="15de0-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15de0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15de0-136">-ResourceGroupName</span></span>
<span data-ttu-id="15de0-137">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15de0-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15de0-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="15de0-138">-SourceVaultId</span></span>
<span data-ttu-id="15de0-139">Идентификатор ресурса для хранилища ключей, содержащий сертификаты.</span><span class="sxs-lookup"><span data-stu-id="15de0-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="15de0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15de0-140">-Confirm</span></span>
<span data-ttu-id="15de0-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15de0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15de0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15de0-142">-WhatIf</span></span>
<span data-ttu-id="15de0-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15de0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15de0-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15de0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15de0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15de0-145">CommonParameters</span></span>
<span data-ttu-id="15de0-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15de0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15de0-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15de0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15de0-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15de0-148">INPUTS</span></span>

### <span data-ttu-id="15de0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="15de0-149">System.String</span></span>

## <span data-ttu-id="15de0-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15de0-150">OUTPUTS</span></span>

### <span data-ttu-id="15de0-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="15de0-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="15de0-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="15de0-152">NOTES</span></span>

## <span data-ttu-id="15de0-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15de0-153">RELATED LINKS</span></span>
