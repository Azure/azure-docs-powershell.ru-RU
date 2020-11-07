---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907045"
---
# <span data-ttu-id="f7492-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f7492-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="f7492-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7492-102">SYNOPSIS</span></span>
<span data-ttu-id="f7492-103">Возвращает или отображает общие файлы хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7492-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="f7492-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7492-104">SYNTAX</span></span>

### <span data-ttu-id="f7492-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7492-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7492-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f7492-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7492-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f7492-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7492-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7492-108">DESCRIPTION</span></span>
<span data-ttu-id="f7492-109">Командлет **Get-AzRmStorageShare** получает или отображает общие файлы хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7492-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="f7492-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7492-110">EXAMPLES</span></span>

### <span data-ttu-id="f7492-111">Пример 1: получение общего файлового хранилища с именем учетной записи хранения и именем общего доступа</span><span class="sxs-lookup"><span data-stu-id="f7492-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="f7492-112">Эта команда возвращает общую файловую систему хранилища с именем учетной записи хранения и именем общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f7492-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="f7492-113">Пример 2: список всех общих файловых ресурсов хранилища для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f7492-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="f7492-114">Эта команда перечисляет все общие файлы хранилища для учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7492-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="f7492-115">Пример 3: получение контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="f7492-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="f7492-116">Эта команда получает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="f7492-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="f7492-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7492-117">PARAMETERS</span></span>

### <span data-ttu-id="f7492-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7492-118">-DefaultProfile</span></span>
<span data-ttu-id="f7492-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7492-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7492-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7492-120">-Name</span></span>
<span data-ttu-id="f7492-121">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="f7492-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7492-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7492-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7492-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7492-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7492-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7492-124">-ResourceId</span></span>
<span data-ttu-id="f7492-125">Введите идентификатор ресурса для общего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="f7492-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7492-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7492-126">-StorageAccount</span></span>
<span data-ttu-id="f7492-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f7492-127">Storage account object</span></span>

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

### <span data-ttu-id="f7492-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7492-128">-StorageAccountName</span></span>
<span data-ttu-id="f7492-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7492-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="f7492-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7492-130">CommonParameters</span></span>
<span data-ttu-id="f7492-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7492-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7492-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7492-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7492-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7492-133">INPUTS</span></span>

### <span data-ttu-id="f7492-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f7492-134">System.String</span></span>

### <span data-ttu-id="f7492-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7492-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f7492-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7492-136">OUTPUTS</span></span>

### <span data-ttu-id="f7492-137">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="f7492-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f7492-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7492-138">NOTES</span></span>

## <span data-ttu-id="f7492-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7492-139">RELATED LINKS</span></span>
