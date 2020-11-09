---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318332"
---
# <span data-ttu-id="755cd-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="755cd-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="755cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="755cd-102">SYNOPSIS</span></span>
<span data-ttu-id="755cd-103">Создает новые учетные данные для учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="755cd-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="755cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="755cd-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="755cd-105">DESCRIPTION</span></span>
<span data-ttu-id="755cd-106">Командлет **New-AzStackEdgeStorageAccountCredential** создает новые учетные данные учетной записи хранилища пограничного устройства в стопке.</span><span class="sxs-lookup"><span data-stu-id="755cd-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="755cd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="755cd-107">EXAMPLES</span></span>

### <span data-ttu-id="755cd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="755cd-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="755cd-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="755cd-109">PARAMETERS</span></span>

### <span data-ttu-id="755cd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="755cd-110">-AsJob</span></span>
<span data-ttu-id="755cd-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="755cd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="755cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755cd-112">-DefaultProfile</span></span>
<span data-ttu-id="755cd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="755cd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755cd-114">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="755cd-114">-DeviceName</span></span>
<span data-ttu-id="755cd-115">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="755cd-115">Device Name</span></span>

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

### <span data-ttu-id="755cd-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="755cd-116">-EncryptionKey</span></span>
<span data-ttu-id="755cd-117">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="755cd-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="755cd-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="755cd-118">-Name</span></span>
<span data-ttu-id="755cd-119">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="755cd-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="755cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="755cd-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="755cd-121">Resource Group Name</span></span>

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

### <span data-ttu-id="755cd-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="755cd-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="755cd-123">предоставление ключа доступа учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="755cd-123">provide storage account access key</span></span>

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

### <span data-ttu-id="755cd-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="755cd-124">-StorageAccountType</span></span>
<span data-ttu-id="755cd-125">Возможно, тип доступа к хранилищу GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="755cd-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="755cd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="755cd-126">-Confirm</span></span>
<span data-ttu-id="755cd-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="755cd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755cd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755cd-128">-WhatIf</span></span>
<span data-ttu-id="755cd-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="755cd-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="755cd-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="755cd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755cd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755cd-131">CommonParameters</span></span>
<span data-ttu-id="755cd-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="755cd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755cd-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="755cd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755cd-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="755cd-134">INPUTS</span></span>

### <span data-ttu-id="755cd-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="755cd-135">None</span></span>

## <span data-ttu-id="755cd-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="755cd-136">OUTPUTS</span></span>

### <span data-ttu-id="755cd-137">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="755cd-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="755cd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="755cd-138">NOTES</span></span>

## <span data-ttu-id="755cd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="755cd-139">RELATED LINKS</span></span>