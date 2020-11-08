---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073150"
---
# <span data-ttu-id="6aa3e-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6aa3e-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="6aa3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6aa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa3e-103">Создание контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="6aa3e-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="6aa3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6aa3e-104">SYNTAX</span></span>

### <span data-ttu-id="6aa3e-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6aa3e-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa3e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6aa3e-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aa3e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aa3e-107">DESCRIPTION</span></span>
<span data-ttu-id="6aa3e-108">Командлет **New-AzRmStorageContainer** создает контейнер BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="6aa3e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6aa3e-109">EXAMPLES</span></span>

### <span data-ttu-id="6aa3e-110">Пример 1: создание контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера с метаданными</span><span class="sxs-lookup"><span data-stu-id="6aa3e-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="6aa3e-111">Эта команда создает контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера с метаданными.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="6aa3e-112">Пример 2: создание контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера с открытым доступом как с BLOB-объектом</span><span class="sxs-lookup"><span data-stu-id="6aa3e-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="6aa3e-113">Эта команда создает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера с открытым доступом в качестве BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="6aa3e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6aa3e-114">PARAMETERS</span></span>

### <span data-ttu-id="6aa3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa3e-115">-DefaultProfile</span></span>
<span data-ttu-id="6aa3e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa3e-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6aa3e-117">-Metadata</span></span>
<span data-ttu-id="6aa3e-118">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="6aa3e-118">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6aa3e-119">-Name</span></span>
<span data-ttu-id="6aa3e-120">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="6aa3e-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3e-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6aa3e-121">-PublicAccess</span></span>
<span data-ttu-id="6aa3e-122">Контейнер PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6aa3e-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="6aa3e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3e-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6aa3e-125">-StorageAccount</span></span>
<span data-ttu-id="6aa3e-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6aa3e-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3e-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6aa3e-127">-StorageAccountName</span></span>
<span data-ttu-id="6aa3e-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aa3e-129">-Confirm</span></span>
<span data-ttu-id="6aa3e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa3e-131">-WhatIf</span></span>
<span data-ttu-id="6aa3e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6aa3e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa3e-134">CommonParameters</span></span>
<span data-ttu-id="6aa3e-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6aa3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa3e-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa3e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa3e-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6aa3e-137">INPUTS</span></span>

### <span data-ttu-id="6aa3e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6aa3e-138">System.String</span></span>

### <span data-ttu-id="6aa3e-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6aa3e-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6aa3e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aa3e-140">OUTPUTS</span></span>

### <span data-ttu-id="6aa3e-141">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="6aa3e-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6aa3e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="6aa3e-142">NOTES</span></span>

## <span data-ttu-id="6aa3e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aa3e-143">RELATED LINKS</span></span>
