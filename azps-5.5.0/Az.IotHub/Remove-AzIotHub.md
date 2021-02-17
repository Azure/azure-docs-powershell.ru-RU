---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234156"
---
# <span data-ttu-id="01ccd-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="01ccd-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="01ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="01ccd-103">Удаляет IotHub.</span><span class="sxs-lookup"><span data-stu-id="01ccd-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="01ccd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01ccd-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ccd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ccd-105">DESCRIPTION</span></span>
<span data-ttu-id="01ccd-106">Удаляет IotHub.</span><span class="sxs-lookup"><span data-stu-id="01ccd-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="01ccd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01ccd-107">EXAMPLES</span></span>

### <span data-ttu-id="01ccd-108">Пример 1. Удаление iotHub</span><span class="sxs-lookup"><span data-stu-id="01ccd-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="01ccd-109">Удаляет IotHub с именем Myiothub.</span><span class="sxs-lookup"><span data-stu-id="01ccd-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="01ccd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01ccd-110">PARAMETERS</span></span>

### <span data-ttu-id="01ccd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ccd-111">-DefaultProfile</span></span>
<span data-ttu-id="01ccd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01ccd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01ccd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="01ccd-113">-Name</span></span>
<span data-ttu-id="01ccd-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="01ccd-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="01ccd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ccd-115">-ResourceGroupName</span></span>
<span data-ttu-id="01ccd-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="01ccd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="01ccd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01ccd-117">-Confirm</span></span>
<span data-ttu-id="01ccd-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01ccd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ccd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ccd-119">-WhatIf</span></span>
<span data-ttu-id="01ccd-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01ccd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ccd-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="01ccd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ccd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ccd-122">CommonParameters</span></span>
<span data-ttu-id="01ccd-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ccd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ccd-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ccd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ccd-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01ccd-125">INPUTS</span></span>

### <span data-ttu-id="01ccd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="01ccd-126">System.String</span></span>

## <span data-ttu-id="01ccd-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01ccd-127">OUTPUTS</span></span>

### <span data-ttu-id="01ccd-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="01ccd-128">System.Void</span></span>

## <span data-ttu-id="01ccd-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01ccd-129">NOTES</span></span>

## <span data-ttu-id="01ccd-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01ccd-130">RELATED LINKS</span></span>
