---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558191"
---
# <span data-ttu-id="e1a0e-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e1a0e-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="e1a0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a0e-103">Возвращает или приводит список контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1a0e-104">SYNTAX</span></span>

### <span data-ttu-id="e1a0e-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1a0e-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1a0e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e1a0e-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a0e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1a0e-107">DESCRIPTION</span></span>
<span data-ttu-id="e1a0e-108">Командлет **Get-AzureRmStorageContainer** получает или приводит список контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="e1a0e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1a0e-109">EXAMPLES</span></span>

### <span data-ttu-id="e1a0e-110">Пример 1: получение контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="e1a0e-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="e1a0e-111">Эта команда получает контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="e1a0e-112">Пример 2: список всех контейнеров больших двоичных объектов хранилища для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e1a0e-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="e1a0e-113">Эта команда перечисляет все контейнеры больших двоичных объектов хранилища для учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="e1a0e-114">Пример 3: получение контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="e1a0e-115">Эта команда получает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="e1a0e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1a0e-116">PARAMETERS</span></span>

### <span data-ttu-id="e1a0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a0e-117">-DefaultProfile</span></span>
<span data-ttu-id="e1a0e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1a0e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1a0e-119">-Name</span></span>
<span data-ttu-id="e1a0e-120">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="e1a0e-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a0e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a0e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1a0e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e1a0e-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1a0e-123">-StorageAccount</span></span>
<span data-ttu-id="e1a0e-124">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e1a0e-124">Storage account object</span></span>

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

### <span data-ttu-id="e1a0e-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e1a0e-125">-StorageAccountName</span></span>
<span data-ttu-id="e1a0e-126">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="e1a0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a0e-127">CommonParameters</span></span>
<span data-ttu-id="e1a0e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1a0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a0e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a0e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a0e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1a0e-130">INPUTS</span></span>

### <span data-ttu-id="e1a0e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e1a0e-131">System.String</span></span>

## <span data-ttu-id="e1a0e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1a0e-132">OUTPUTS</span></span>

### <span data-ttu-id="e1a0e-133">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="e1a0e-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e1a0e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1a0e-134">NOTES</span></span>

## <span data-ttu-id="e1a0e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1a0e-135">RELATED LINKS</span></span>

