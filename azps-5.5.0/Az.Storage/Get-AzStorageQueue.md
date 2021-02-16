---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212265"
---
# <span data-ttu-id="7d814-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7d814-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="7d814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d814-102">SYNOPSIS</span></span>
<span data-ttu-id="7d814-103">Список очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="7d814-103">Lists storage queues.</span></span>

## <span data-ttu-id="7d814-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d814-104">SYNTAX</span></span>

### <span data-ttu-id="7d814-105">QueueName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d814-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d814-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="7d814-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d814-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d814-107">DESCRIPTION</span></span>
<span data-ttu-id="7d814-108">С **помощью cmdlet Get-AzStorageQueue** можно выведет список очередей хранилища, связанных с учетной записью хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7d814-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="7d814-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d814-109">EXAMPLES</span></span>

### <span data-ttu-id="7d814-110">Пример 1. Список всех очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="7d814-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="7d814-111">Эта команда возвращает список всех очередей хранилища для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7d814-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="7d814-112">Пример 2. Список очередей хранилища Azure с использованием подстрок</span><span class="sxs-lookup"><span data-stu-id="7d814-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="7d814-113">Эта команда использует подстройки для получения списка очередей хранилища, названия которых начинаются с очереди.</span><span class="sxs-lookup"><span data-stu-id="7d814-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="7d814-114">Пример 3. Список очередей хранилища Azure с помощью префикса имени очереди</span><span class="sxs-lookup"><span data-stu-id="7d814-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="7d814-115">В этом примере параметр *Prefix* используется для получения списка очередей хранилища, имена которых начинаются с очереди.</span><span class="sxs-lookup"><span data-stu-id="7d814-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="7d814-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d814-116">PARAMETERS</span></span>

### <span data-ttu-id="7d814-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7d814-117">-Context</span></span>
<span data-ttu-id="7d814-118">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7d814-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7d814-119">Его можно создать с помощью **cmdlet New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="7d814-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d814-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d814-120">-DefaultProfile</span></span>
<span data-ttu-id="7d814-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d814-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d814-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7d814-122">-Name</span></span>
<span data-ttu-id="7d814-123">Указывает имя.</span><span class="sxs-lookup"><span data-stu-id="7d814-123">Specifies a name.</span></span>
<span data-ttu-id="7d814-124">Если имя не указано, получается список всех очередей.</span><span class="sxs-lookup"><span data-stu-id="7d814-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="7d814-125">Если задано полное или частичное имя, командлет получает все очереди, которые соответствуют шаблону имени.</span><span class="sxs-lookup"><span data-stu-id="7d814-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d814-126">-Префикс</span><span class="sxs-lookup"><span data-stu-id="7d814-126">-Prefix</span></span>
<span data-ttu-id="7d814-127">Указывает префикс, используемый в именах очередей, которые вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="7d814-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d814-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d814-128">CommonParameters</span></span>
<span data-ttu-id="7d814-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d814-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d814-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d814-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d814-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d814-131">INPUTS</span></span>

### <span data-ttu-id="7d814-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7d814-132">System.String</span></span>

### <span data-ttu-id="7d814-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d814-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7d814-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d814-134">OUTPUTS</span></span>

### <span data-ttu-id="7d814-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7d814-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="7d814-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d814-136">NOTES</span></span>

## <span data-ttu-id="7d814-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d814-137">RELATED LINKS</span></span>

[<span data-ttu-id="7d814-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7d814-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="7d814-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7d814-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


