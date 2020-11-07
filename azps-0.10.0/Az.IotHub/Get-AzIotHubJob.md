---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 36c336f516cf2621a64a6e0e353e93e7defa03b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910344"
---
# <span data-ttu-id="f6c47-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="f6c47-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="f6c47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6c47-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c47-103">Получает сведения о задании IotHub.</span><span class="sxs-lookup"><span data-stu-id="f6c47-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="f6c47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6c47-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c47-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c47-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c47-106">Получает сведения о задании IotHub.</span><span class="sxs-lookup"><span data-stu-id="f6c47-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="f6c47-107">Задание IotHub создается, когда операция импорта или экспорта инициализируется с помощью команд New-AzIotHubExportDevices или New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="f6c47-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="f6c47-108">Вы можете либо вывести список всех заданий, либо отфильтровать задания по идентификатору задания.</span><span class="sxs-lookup"><span data-stu-id="f6c47-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="f6c47-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6c47-109">EXAMPLES</span></span>

### <span data-ttu-id="f6c47-110">Пример 1. список всех заданий</span><span class="sxs-lookup"><span data-stu-id="f6c47-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f6c47-111">Получает все задания для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f6c47-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="f6c47-112">Пример 2 получение определенного задания</span><span class="sxs-lookup"><span data-stu-id="f6c47-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="f6c47-113">Получение сведений о задании с идентификатором "3630fc31-4caa-43e8-a232-ea0577221cb2" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f6c47-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f6c47-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6c47-114">PARAMETERS</span></span>

### <span data-ttu-id="f6c47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c47-115">-DefaultProfile</span></span>
<span data-ttu-id="f6c47-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6c47-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6c47-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="f6c47-117">-JobId</span></span>
<span data-ttu-id="f6c47-118">Идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="f6c47-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c47-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6c47-119">-Name</span></span>
<span data-ttu-id="f6c47-120">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f6c47-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="f6c47-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6c47-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6c47-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f6c47-122">Resource Group Name</span></span>

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

### <span data-ttu-id="f6c47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c47-123">CommonParameters</span></span>
<span data-ttu-id="f6c47-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6c47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c47-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c47-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c47-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6c47-126">INPUTS</span></span>

### <span data-ttu-id="f6c47-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f6c47-127">System.String</span></span>

## <span data-ttu-id="f6c47-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c47-128">OUTPUTS</span></span>

### <span data-ttu-id="f6c47-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="f6c47-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="f6c47-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6c47-130">NOTES</span></span>

## <span data-ttu-id="f6c47-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6c47-131">RELATED LINKS</span></span>
