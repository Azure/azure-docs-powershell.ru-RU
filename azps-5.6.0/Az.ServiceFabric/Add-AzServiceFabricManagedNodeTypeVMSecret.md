---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 35d755bc117ccc4379be8d7344d8e7170594d555
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969795"
---
# <span data-ttu-id="ba9a9-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="ba9a9-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="ba9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9a9-103">Добавьте секрет сертификата к типу узла.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="ba9a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba9a9-104">SYNTAX</span></span>

### <span data-ttu-id="ba9a9-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba9a9-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9a9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ba9a9-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9a9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba9a9-107">DESCRIPTION</span></span>
<span data-ttu-id="ba9a9-108">Добавьте секрет сертификата к типу узла.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="ba9a9-109">Секрет должен храниться в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="ba9a9-110">Дополнительные сведения, связанные с хранилищем ключей, см. в подмносях "Что такое хранилище ключей Azure"?</span><span class="sxs-lookup"><span data-stu-id="ba9a9-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="ba9a9-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="ba9a9-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="ba9a9-112">Дополнительные сведения о Set-AzKeyVaultSecret см. в Microsoft Developer Network Службе управления ключами https://msdn.microsoft.com/library/azure/dn868052.aspx) Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="ba9a9-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba9a9-113">EXAMPLES</span></span>

### <span data-ttu-id="ba9a9-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba9a9-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="ba9a9-115">Эта запятая добавляет секрет сертификата из заданного ключа и секретного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="ba9a9-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ba9a9-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="ba9a9-117">Эта запятая добавляет секрет сертификата из keyvault и указанного секретного идентификатора с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="ba9a9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba9a9-118">PARAMETERS</span></span>

### <span data-ttu-id="ba9a9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba9a9-119">-AsJob</span></span>
<span data-ttu-id="ba9a9-120">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ba9a9-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="ba9a9-121">-CertificateStore</span></span>
<span data-ttu-id="ba9a9-122">Указывает хранилище сертификатов на виртуальной машине, в которое нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="ba9a9-123">Указанное хранилище сертификатов неявно указывается в учетной записи LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="ba9a9-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ba9a9-124">-CertificateUrl</span></span>
<span data-ttu-id="ba9a9-125">Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="ba9a9-126">Чтобы узнать, как добавить секрет в хранилище ключей, см. также: "Добавление ключа или секрета в \[ хранилище \] ключей" https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) (.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="ba9a9-127">В этом случае сертификат должен быть кодировки Base64 для следующего объекта JSON, который закодирован в UTF-8: \<br\> \<br\> { \<br\> "data":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="ba9a9-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="ba9a9-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba9a9-128">-ClusterName</span></span>
<span data-ttu-id="ba9a9-129">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ba9a9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9a9-130">-DefaultProfile</span></span>
<span data-ttu-id="ba9a9-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9a9-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba9a9-132">-InputObject</span></span>
<span data-ttu-id="ba9a9-133">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="ba9a9-133">Node Type resource</span></span>

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

### <span data-ttu-id="ba9a9-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ba9a9-134">-Name</span></span>
<span data-ttu-id="ba9a9-135">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="ba9a9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9a9-136">-ResourceGroupName</span></span>
<span data-ttu-id="ba9a9-137">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ba9a9-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ba9a9-138">-SourceVaultId</span></span>
<span data-ttu-id="ba9a9-139">ИД ресурса хранилища ключа, содержащий сертификаты.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="ba9a9-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba9a9-140">-Confirm</span></span>
<span data-ttu-id="ba9a9-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9a9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9a9-142">-WhatIf</span></span>
<span data-ttu-id="ba9a9-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba9a9-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9a9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9a9-145">CommonParameters</span></span>
<span data-ttu-id="ba9a9-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9a9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9a9-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba9a9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9a9-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba9a9-148">INPUTS</span></span>

### <span data-ttu-id="ba9a9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ba9a9-149">System.String</span></span>

## <span data-ttu-id="ba9a9-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba9a9-150">OUTPUTS</span></span>

### <span data-ttu-id="ba9a9-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ba9a9-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="ba9a9-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba9a9-152">NOTES</span></span>

## <span data-ttu-id="ba9a9-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba9a9-153">RELATED LINKS</span></span>
