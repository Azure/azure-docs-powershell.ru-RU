---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221937"
---
# <span data-ttu-id="9dd89-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9dd89-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9dd89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd89-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd89-103">Создает учетные данные для учетной записи edge storage на устройстве.</span><span class="sxs-lookup"><span data-stu-id="9dd89-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="9dd89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9dd89-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dd89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dd89-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd89-106">Для устройства Stack Edge с новыми учетными данными учетной записи границы создается новый учетный данные для **AzStackEdgeStorageAccountCredential.**</span><span class="sxs-lookup"><span data-stu-id="9dd89-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="9dd89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9dd89-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9dd89-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="9dd89-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dd89-109">PARAMETERS</span></span>

### <span data-ttu-id="9dd89-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dd89-110">-AsJob</span></span>
<span data-ttu-id="9dd89-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9dd89-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dd89-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd89-112">-DefaultProfile</span></span>
<span data-ttu-id="9dd89-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd89-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd89-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9dd89-114">-DeviceName</span></span>
<span data-ttu-id="9dd89-115">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="9dd89-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd89-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9dd89-116">-EncryptionKey</span></span>
<span data-ttu-id="9dd89-117">Ключ шифрования устройства Edge</span><span class="sxs-lookup"><span data-stu-id="9dd89-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9dd89-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9dd89-118">-Name</span></span>
<span data-ttu-id="9dd89-119">Имя используемой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9dd89-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd89-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd89-120">-ResourceGroupName</span></span>
<span data-ttu-id="9dd89-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9dd89-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd89-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="9dd89-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="9dd89-123">предоставление ключа доступа к учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9dd89-123">provide storage account access key</span></span>

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

### <span data-ttu-id="9dd89-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9dd89-124">-StorageAccountType</span></span>
<span data-ttu-id="9dd89-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="9dd89-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="9dd89-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dd89-126">-Confirm</span></span>
<span data-ttu-id="9dd89-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9dd89-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd89-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd89-128">-WhatIf</span></span>
<span data-ttu-id="9dd89-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dd89-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dd89-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9dd89-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd89-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd89-131">CommonParameters</span></span>
<span data-ttu-id="9dd89-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd89-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd89-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dd89-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd89-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd89-134">INPUTS</span></span>

### <span data-ttu-id="9dd89-135">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd89-135">None</span></span>

## <span data-ttu-id="9dd89-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd89-136">OUTPUTS</span></span>

### <span data-ttu-id="9dd89-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9dd89-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9dd89-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9dd89-138">NOTES</span></span>

## <span data-ttu-id="9dd89-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dd89-139">RELATED LINKS</span></span>
