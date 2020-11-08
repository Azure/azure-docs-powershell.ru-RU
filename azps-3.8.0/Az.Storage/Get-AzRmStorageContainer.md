---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066774"
---
# <span data-ttu-id="06aa3-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="06aa3-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="06aa3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="06aa3-103">Возвращает или приводит список контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="06aa3-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="06aa3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06aa3-104">SYNTAX</span></span>

### <span data-ttu-id="06aa3-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06aa3-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06aa3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="06aa3-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06aa3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06aa3-107">DESCRIPTION</span></span>
<span data-ttu-id="06aa3-108">Командлет **Get-AzRmStorageContainer** получает или приводит список контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="06aa3-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="06aa3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06aa3-109">EXAMPLES</span></span>

### <span data-ttu-id="06aa3-110">Пример 1: получение контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="06aa3-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="06aa3-111">Эта команда получает контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="06aa3-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="06aa3-112">Пример 2: список всех контейнеров больших двоичных объектов хранилища для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="06aa3-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="06aa3-113">Эта команда перечисляет все контейнеры больших двоичных объектов хранилища для учетной записи хранения с именем учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="06aa3-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="06aa3-114">Пример 3: получение контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="06aa3-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="06aa3-115">Эта команда получает контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="06aa3-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="06aa3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06aa3-116">PARAMETERS</span></span>

### <span data-ttu-id="06aa3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06aa3-117">-AsJob</span></span>
<span data-ttu-id="06aa3-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="06aa3-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06aa3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06aa3-119">-DefaultProfile</span></span>
<span data-ttu-id="06aa3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06aa3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06aa3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06aa3-121">-Name</span></span>
<span data-ttu-id="06aa3-122">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="06aa3-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06aa3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06aa3-123">-ResourceGroupName</span></span>
<span data-ttu-id="06aa3-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06aa3-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="06aa3-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="06aa3-125">-StorageAccount</span></span>
<span data-ttu-id="06aa3-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="06aa3-126">Storage account object</span></span>

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

### <span data-ttu-id="06aa3-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06aa3-127">-StorageAccountName</span></span>
<span data-ttu-id="06aa3-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="06aa3-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="06aa3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06aa3-129">CommonParameters</span></span>
<span data-ttu-id="06aa3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06aa3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06aa3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06aa3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06aa3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06aa3-132">INPUTS</span></span>

### <span data-ttu-id="06aa3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06aa3-133">System.String</span></span>

### <span data-ttu-id="06aa3-134">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06aa3-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="06aa3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06aa3-135">OUTPUTS</span></span>

### <span data-ttu-id="06aa3-136">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="06aa3-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="06aa3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="06aa3-137">NOTES</span></span>

## <span data-ttu-id="06aa3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06aa3-138">RELATED LINKS</span></span>
