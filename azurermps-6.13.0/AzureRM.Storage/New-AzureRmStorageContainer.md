---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558195"
---
# <span data-ttu-id="9832c-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9832c-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="9832c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9832c-102">SYNOPSIS</span></span>
<span data-ttu-id="9832c-103">Создание контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="9832c-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9832c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9832c-104">SYNTAX</span></span>

### <span data-ttu-id="9832c-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9832c-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9832c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9832c-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9832c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9832c-107">DESCRIPTION</span></span>
<span data-ttu-id="9832c-108">Командлет **New-AzureRmStorageContainer** создает контейнер BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="9832c-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="9832c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9832c-109">EXAMPLES</span></span>

### <span data-ttu-id="9832c-110">Пример 1: создание контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера с метаданными</span><span class="sxs-lookup"><span data-stu-id="9832c-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="9832c-111">Эта команда создает контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера с метаданными.</span><span class="sxs-lookup"><span data-stu-id="9832c-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="9832c-112">Пример 2: создание контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера с открытым доступом как с BLOB-объектом</span><span class="sxs-lookup"><span data-stu-id="9832c-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="9832c-113">Эта команда создает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера с открытым доступом в качестве BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="9832c-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="9832c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9832c-114">PARAMETERS</span></span>

### <span data-ttu-id="9832c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9832c-115">-DefaultProfile</span></span>
<span data-ttu-id="9832c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9832c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9832c-117">-Metadata</span></span>
<span data-ttu-id="9832c-118">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="9832c-118">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9832c-119">-Name</span></span>
<span data-ttu-id="9832c-120">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="9832c-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="9832c-121">-PublicAccess</span></span>
<span data-ttu-id="9832c-122">Контейнер PublicAccess</span><span class="sxs-lookup"><span data-stu-id="9832c-122">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9832c-123">-ResourceGroupName</span></span>
<span data-ttu-id="9832c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9832c-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9832c-125">-StorageAccount</span></span>
<span data-ttu-id="9832c-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9832c-126">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9832c-127">-StorageAccountName</span></span>
<span data-ttu-id="9832c-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9832c-128">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9832c-129">-Confirm</span></span>
<span data-ttu-id="9832c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9832c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9832c-131">-WhatIf</span></span>
<span data-ttu-id="9832c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9832c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9832c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9832c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9832c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9832c-134">CommonParameters</span></span>
<span data-ttu-id="9832c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9832c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9832c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9832c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9832c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9832c-137">INPUTS</span></span>

### <span data-ttu-id="9832c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9832c-138">System.String</span></span>

## <span data-ttu-id="9832c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9832c-139">OUTPUTS</span></span>

### <span data-ttu-id="9832c-140">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="9832c-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9832c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9832c-141">NOTES</span></span>

## <span data-ttu-id="9832c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9832c-142">RELATED LINKS</span></span>

