---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219764"
---
# <span data-ttu-id="7fb1f-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="7fb1f-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="7fb1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb1f-103">Получает сведения о заданиях IotHub.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="7fb1f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7fb1f-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fb1f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb1f-106">Получает сведения о заданиях IotHub.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="7fb1f-107">Задание IotHub создается при инициализации операции импорта или экспорта с New-AzIotHubExportDevices или New-AzIotHubImportDevices экспорта.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="7fb1f-108">Вы можете перечислить все задания или отфильтровать их по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="7fb1f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7fb1f-109">EXAMPLES</span></span>

### <span data-ttu-id="7fb1f-110">Пример 1. Список всех заданий</span><span class="sxs-lookup"><span data-stu-id="7fb1f-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7fb1f-111">Все задания для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7fb1f-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="7fb1f-112">Пример 2. Получить задание</span><span class="sxs-lookup"><span data-stu-id="7fb1f-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="7fb1f-113">Сведения о работе с идентификатором 3630fc31-4caa-43e8-a232-ea0577221cb2" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7fb1f-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7fb1f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fb1f-114">PARAMETERS</span></span>

### <span data-ttu-id="7fb1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb1f-115">-DefaultProfile</span></span>
<span data-ttu-id="7fb1f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7fb1f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fb1f-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="7fb1f-117">-JobId</span></span>
<span data-ttu-id="7fb1f-118">Идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="7fb1f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7fb1f-119">-Name</span></span>
<span data-ttu-id="7fb1f-120">Имя концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7fb1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7fb1f-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7fb1f-122">Resource Group Name</span></span>

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

### <span data-ttu-id="7fb1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb1f-123">CommonParameters</span></span>
<span data-ttu-id="7fb1f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb1f-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb1f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb1f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fb1f-126">INPUTS</span></span>

### <span data-ttu-id="7fb1f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7fb1f-127">System.String</span></span>

## <span data-ttu-id="7fb1f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7fb1f-128">OUTPUTS</span></span>

### <span data-ttu-id="7fb1f-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="7fb1f-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="7fb1f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7fb1f-130">NOTES</span></span>

## <span data-ttu-id="7fb1f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fb1f-131">RELATED LINKS</span></span>
