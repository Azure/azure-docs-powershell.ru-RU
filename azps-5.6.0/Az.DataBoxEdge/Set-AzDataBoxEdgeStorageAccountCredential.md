---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 214b43148020b2884013a45f26b4a03cd4ea3736
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971283"
---
# <span data-ttu-id="5fc9f-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5fc9f-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5fc9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc9f-103">Задает учетные данные учетной записи хранения для устройства.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="5fc9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fc9f-104">SYNTAX</span></span>

### <span data-ttu-id="5fc9f-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fc9f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc9f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fc9f-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc9f-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fc9f-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fc9f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fc9f-108">DESCRIPTION</span></span>
<span data-ttu-id="5fc9f-109">**Cmdlet Set-AzDataBoxEdgeStorageAccountCredential** обновляет учетную запись хранения, соответствующую учетной записи хранения на устройстве Edge Data Box.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="5fc9f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fc9f-110">EXAMPLES</span></span>

### <span data-ttu-id="5fc9f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fc9f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="5fc9f-112">Поворот ключей доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="5fc9f-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="5fc9f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fc9f-113">PARAMETERS</span></span>

### <span data-ttu-id="5fc9f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fc9f-114">-AsJob</span></span>
<span data-ttu-id="5fc9f-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5fc9f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fc9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc9f-116">-DefaultProfile</span></span>
<span data-ttu-id="5fc9f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fc9f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5fc9f-118">-DeviceName</span></span>
<span data-ttu-id="5fc9f-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="5fc9f-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5fc9f-120">-EncryptionKey</span></span>
<span data-ttu-id="5fc9f-121">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="5fc9f-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fc9f-122">-InputObject</span></span>
<span data-ttu-id="5fc9f-123">Объект Input</span><span class="sxs-lookup"><span data-stu-id="5fc9f-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5fc9f-124">-Name</span></span>
<span data-ttu-id="5fc9f-125">Имя используемой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="5fc9f-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc9f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5fc9f-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5fc9f-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc9f-128">-ResourceId</span></span>
<span data-ttu-id="5fc9f-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc9f-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="5fc9f-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="5fc9f-131">предоставление ключа доступа к учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="5fc9f-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc9f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fc9f-132">-Confirm</span></span>
<span data-ttu-id="5fc9f-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fc9f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fc9f-134">-WhatIf</span></span>
<span data-ttu-id="5fc9f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fc9f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fc9f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc9f-137">CommonParameters</span></span>
<span data-ttu-id="5fc9f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc9f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc9f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fc9f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc9f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fc9f-140">INPUTS</span></span>

### <span data-ttu-id="5fc9f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc9f-141">System.String</span></span>

### <span data-ttu-id="5fc9f-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5fc9f-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5fc9f-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fc9f-143">OUTPUTS</span></span>

### <span data-ttu-id="5fc9f-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5fc9f-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5fc9f-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fc9f-145">NOTES</span></span>

## <span data-ttu-id="5fc9f-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fc9f-146">RELATED LINKS</span></span>
