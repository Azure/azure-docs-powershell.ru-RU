---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230684"
---
# <span data-ttu-id="11883-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="11883-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="11883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11883-102">SYNOPSIS</span></span>
<span data-ttu-id="11883-103">Создает учетные данные для учетной записи edge storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="11883-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="11883-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11883-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11883-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11883-105">DESCRIPTION</span></span>
<span data-ttu-id="11883-106">Для устройства Edge Data Box с новыми учетными данными **AzDataBoxEdgeStorageAccountCredential** создается учетная запись границы хранилища.</span><span class="sxs-lookup"><span data-stu-id="11883-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="11883-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11883-107">EXAMPLES</span></span>

### <span data-ttu-id="11883-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11883-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="11883-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11883-109">PARAMETERS</span></span>

### <span data-ttu-id="11883-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11883-110">-AsJob</span></span>
<span data-ttu-id="11883-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="11883-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11883-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11883-112">-DefaultProfile</span></span>
<span data-ttu-id="11883-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11883-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11883-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="11883-114">-DeviceName</span></span>
<span data-ttu-id="11883-115">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="11883-115">Device Name</span></span>

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

### <span data-ttu-id="11883-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="11883-116">-EncryptionKey</span></span>
<span data-ttu-id="11883-117">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="11883-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="11883-118">-Name</span><span class="sxs-lookup"><span data-stu-id="11883-118">-Name</span></span>
<span data-ttu-id="11883-119">Имя используемой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="11883-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11883-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11883-120">-ResourceGroupName</span></span>
<span data-ttu-id="11883-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="11883-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11883-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="11883-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="11883-123">предоставление ключа доступа к учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="11883-123">provide storage account access key</span></span>

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

### <span data-ttu-id="11883-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="11883-124">-StorageAccountType</span></span>
<span data-ttu-id="11883-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="11883-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="11883-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11883-126">-Confirm</span></span>
<span data-ttu-id="11883-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="11883-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11883-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11883-128">-WhatIf</span></span>
<span data-ttu-id="11883-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11883-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11883-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="11883-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11883-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11883-131">CommonParameters</span></span>
<span data-ttu-id="11883-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11883-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11883-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11883-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11883-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11883-134">INPUTS</span></span>

### <span data-ttu-id="11883-135">Нет</span><span class="sxs-lookup"><span data-stu-id="11883-135">None</span></span>

## <span data-ttu-id="11883-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11883-136">OUTPUTS</span></span>

### <span data-ttu-id="11883-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="11883-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="11883-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11883-138">NOTES</span></span>

## <span data-ttu-id="11883-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11883-139">RELATED LINKS</span></span>
