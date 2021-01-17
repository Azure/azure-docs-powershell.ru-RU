---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417132"
---
# <span data-ttu-id="27e08-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="27e08-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="27e08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27e08-102">SYNOPSIS</span></span>
<span data-ttu-id="27e08-103">Возвращает registryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="27e08-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="27e08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27e08-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27e08-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27e08-105">DESCRIPTION</span></span>
<span data-ttu-id="27e08-106">Возвращает registryStatistics для IotHub.</span><span class="sxs-lookup"><span data-stu-id="27e08-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="27e08-107">Это сведения об общем количестве включенных, включенных и отключенных устройств в IotHub.</span><span class="sxs-lookup"><span data-stu-id="27e08-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="27e08-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27e08-108">EXAMPLES</span></span>

### <span data-ttu-id="27e08-109">Пример 1. Получить RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="27e08-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="27e08-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span><span class="sxs-lookup"><span data-stu-id="27e08-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="27e08-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27e08-111">PARAMETERS</span></span>

### <span data-ttu-id="27e08-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e08-112">-DefaultProfile</span></span>
<span data-ttu-id="27e08-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="27e08-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27e08-114">-Name</span><span class="sxs-lookup"><span data-stu-id="27e08-114">-Name</span></span>
<span data-ttu-id="27e08-115">Имя концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="27e08-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="27e08-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e08-116">-ResourceGroupName</span></span>
<span data-ttu-id="27e08-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="27e08-117">Resource Group Name</span></span>

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

### <span data-ttu-id="27e08-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e08-118">CommonParameters</span></span>
<span data-ttu-id="27e08-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e08-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e08-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e08-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e08-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27e08-121">INPUTS</span></span>

### <span data-ttu-id="27e08-122">System.String</span><span class="sxs-lookup"><span data-stu-id="27e08-122">System.String</span></span>

## <span data-ttu-id="27e08-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27e08-123">OUTPUTS</span></span>

### <span data-ttu-id="27e08-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="27e08-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="27e08-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27e08-125">NOTES</span></span>

## <span data-ttu-id="27e08-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27e08-126">RELATED LINKS</span></span>
