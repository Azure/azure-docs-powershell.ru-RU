---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406996"
---
# <span data-ttu-id="24b6f-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="24b6f-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="24b6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="24b6f-103">Создание задания для устройств экспорта.</span><span class="sxs-lookup"><span data-stu-id="24b6f-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="24b6f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24b6f-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b6f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="24b6f-106">Создание задания экспорта устройств для IotHub.</span><span class="sxs-lookup"><span data-stu-id="24b6f-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="24b6f-107">При этом все устройства будут экспортироваться в указанный контейнер.</span><span class="sxs-lookup"><span data-stu-id="24b6f-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="24b6f-108">О том, как создать URI SAS, можно узнать в следующей статье.</span><span class="sxs-lookup"><span data-stu-id="24b6f-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="24b6f-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="24b6f-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="24b6f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24b6f-110">EXAMPLES</span></span>

### <span data-ttu-id="24b6f-111">Пример 1. Проблема с запросом на экспорт устройства.</span><span class="sxs-lookup"><span data-stu-id="24b6f-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="24b6f-112">Создает новый запрос на экспорт устройства для IotHub с исключением ключей.</span><span class="sxs-lookup"><span data-stu-id="24b6f-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="24b6f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24b6f-113">PARAMETERS</span></span>

### <span data-ttu-id="24b6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b6f-114">-DefaultProfile</span></span>
<span data-ttu-id="24b6f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24b6f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24b6f-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="24b6f-116">-ExcludeKeys</span></span>
<span data-ttu-id="24b6f-117">Позволяет экспортировать устройства без ключей.</span><span class="sxs-lookup"><span data-stu-id="24b6f-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="24b6f-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="24b6f-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="24b6f-119">Uri для экспорта BLOB-ля.</span><span class="sxs-lookup"><span data-stu-id="24b6f-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="24b6f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="24b6f-120">-Name</span></span>
<span data-ttu-id="24b6f-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="24b6f-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="24b6f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b6f-122">-ResourceGroupName</span></span>
<span data-ttu-id="24b6f-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="24b6f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="24b6f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24b6f-124">-Confirm</span></span>
<span data-ttu-id="24b6f-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="24b6f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b6f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b6f-126">-WhatIf</span></span>
<span data-ttu-id="24b6f-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24b6f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b6f-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="24b6f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24b6f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b6f-129">CommonParameters</span></span>
<span data-ttu-id="24b6f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b6f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b6f-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b6f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b6f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24b6f-132">INPUTS</span></span>

### <span data-ttu-id="24b6f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="24b6f-133">System.String</span></span>

## <span data-ttu-id="24b6f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24b6f-134">OUTPUTS</span></span>

### <span data-ttu-id="24b6f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="24b6f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="24b6f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24b6f-136">NOTES</span></span>

## <span data-ttu-id="24b6f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24b6f-137">RELATED LINKS</span></span>
