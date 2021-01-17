---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: bb1b5579869c7142bcf6cbe168ff10aaa9b7e083
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328162"
---
# <span data-ttu-id="a579e-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="a579e-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="a579e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a579e-102">SYNOPSIS</span></span>
<span data-ttu-id="a579e-103">Создает задание для устройств импорта.</span><span class="sxs-lookup"><span data-stu-id="a579e-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="a579e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a579e-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a579e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a579e-105">DESCRIPTION</span></span>
<span data-ttu-id="a579e-106">Создает задание для устройств импорта для IotHub.</span><span class="sxs-lookup"><span data-stu-id="a579e-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="a579e-107">Все устройства будут импортироваться в IotHub из указанного контейнера.</span><span class="sxs-lookup"><span data-stu-id="a579e-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="a579e-108">О том, как создать URI SAS, можно узнать в следующей статье.</span><span class="sxs-lookup"><span data-stu-id="a579e-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a579e-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a579e-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a579e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a579e-110">EXAMPLES</span></span>

### <span data-ttu-id="a579e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a579e-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="a579e-112">Создает запрос на импорт устройства для IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a579e-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="a579e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a579e-113">PARAMETERS</span></span>

### <span data-ttu-id="a579e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a579e-114">-DefaultProfile</span></span>
<span data-ttu-id="a579e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a579e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a579e-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a579e-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="a579e-117">Input BLOB Container Uri для FileUpload</span><span class="sxs-lookup"><span data-stu-id="a579e-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a579e-118">-Name</span></span>
<span data-ttu-id="a579e-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="a579e-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="a579e-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a579e-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="a579e-121">Uri, на который нужно вписать выходные данные.</span><span class="sxs-lookup"><span data-stu-id="a579e-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a579e-122">-ResourceGroupName</span></span>
<span data-ttu-id="a579e-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a579e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a579e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a579e-124">-Confirm</span></span>
<span data-ttu-id="a579e-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a579e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a579e-126">-WhatIf</span></span>
<span data-ttu-id="a579e-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a579e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a579e-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a579e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a579e-129">CommonParameters</span></span>
<span data-ttu-id="a579e-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a579e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a579e-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a579e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a579e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a579e-132">INPUTS</span></span>

### <span data-ttu-id="a579e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a579e-133">System.String</span></span>

## <span data-ttu-id="a579e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a579e-134">OUTPUTS</span></span>

### <span data-ttu-id="a579e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a579e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a579e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a579e-136">NOTES</span></span>

## <span data-ttu-id="a579e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a579e-137">RELATED LINKS</span></span>
