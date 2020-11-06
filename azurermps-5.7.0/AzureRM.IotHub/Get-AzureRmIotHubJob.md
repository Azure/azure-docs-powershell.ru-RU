---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: daacefe94d694a6d6288e4c1ccd0f6b05ad1e582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564872"
---
# <span data-ttu-id="b5f3b-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="b5f3b-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="b5f3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f3b-103">Получает сведения о задании IotHub.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5f3b-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5f3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f3b-106">Получает сведения о задании IotHub.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="b5f3b-107">Задание IotHub создается в том случае, если операция импорта или экспорта initialted с помощью команд New-AzureRmIotHubExportDevices или New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="b5f3b-108">Вы можете либо вывести список всех заданий, либо отфильтровать задания по идентификатору задания.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="b5f3b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5f3b-109">EXAMPLES</span></span>

### <span data-ttu-id="b5f3b-110">Пример 1. список всех заданий</span><span class="sxs-lookup"><span data-stu-id="b5f3b-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b5f3b-111">Получает все задания для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b5f3b-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="b5f3b-112">Пример 2 получение определенного задания</span><span class="sxs-lookup"><span data-stu-id="b5f3b-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="b5f3b-113">Получение сведений о задании с идентификатором "3630fc31-4caa-43e8-a232-ea0577221cb2" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b5f3b-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b5f3b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5f3b-114">PARAMETERS</span></span>

### <span data-ttu-id="b5f3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f3b-115">-DefaultProfile</span></span>
<span data-ttu-id="b5f3b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b5f3b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5f3b-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="b5f3b-117">-JobId</span></span>
<span data-ttu-id="b5f3b-118">Идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-118">The Job Identifier.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5f3b-119">-Name</span></span>
<span data-ttu-id="b5f3b-120">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-120">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5f3b-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b5f3b-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f3b-123">CommonParameters</span></span>
<span data-ttu-id="b5f3b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5f3b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f3b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f3b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f3b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5f3b-126">INPUTS</span></span>

### <span data-ttu-id="b5f3b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b5f3b-127">System.String</span></span>

## <span data-ttu-id="b5f3b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5f3b-128">OUTPUTS</span></span>

### <span data-ttu-id="b5f3b-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="b5f3b-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="b5f3b-130">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="b5f3b-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="b5f3b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5f3b-131">NOTES</span></span>

## <span data-ttu-id="b5f3b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5f3b-132">RELATED LINKS</span></span>

