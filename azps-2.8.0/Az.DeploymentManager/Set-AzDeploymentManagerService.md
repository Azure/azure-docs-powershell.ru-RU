---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: 28dc0bd04484823636398b828922fbb79db24672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721107"
---
# <span data-ttu-id="b0047-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b0047-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="b0047-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0047-102">SYNOPSIS</span></span>
<span data-ttu-id="b0047-103">Обновляет службу.</span><span class="sxs-lookup"><span data-stu-id="b0047-103">Updates the service.</span></span>

## <span data-ttu-id="b0047-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0047-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0047-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0047-105">DESCRIPTION</span></span>
<span data-ttu-id="b0047-106">Командлет **Set-AzDeploymentManagerService** обновляет службу с помощью указанного объекта службы.</span><span class="sxs-lookup"><span data-stu-id="b0047-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="b0047-107">Командлет возвращает обновленный объект службы.</span><span class="sxs-lookup"><span data-stu-id="b0047-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="b0047-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0047-108">EXAMPLES</span></span>

### <span data-ttu-id="b0047-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0047-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="b0047-110">Эта команда обновляет службу, имя которой, имя топологии службы и ResourceGroup, совпадают со свойствами Name, ServiceTopologyName и ResourceGroupName для $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="b0047-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="b0047-111">Служба будет обновлена до свойств, заданных в $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="b0047-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="b0047-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0047-112">PARAMETERS</span></span>

### <span data-ttu-id="b0047-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0047-113">-DefaultProfile</span></span>
<span data-ttu-id="b0047-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0047-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0047-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0047-115">-InputObject</span></span>
<span data-ttu-id="b0047-116">Объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b0047-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0047-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0047-117">-Confirm</span></span>
<span data-ttu-id="b0047-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b0047-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0047-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0047-119">-WhatIf</span></span>
<span data-ttu-id="b0047-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b0047-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0047-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b0047-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0047-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0047-122">CommonParameters</span></span>
<span data-ttu-id="b0047-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0047-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0047-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0047-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0047-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0047-125">INPUTS</span></span>

### <span data-ttu-id="b0047-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="b0047-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="b0047-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0047-127">OUTPUTS</span></span>

### <span data-ttu-id="b0047-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="b0047-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="b0047-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0047-129">NOTES</span></span>

## <span data-ttu-id="b0047-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0047-130">RELATED LINKS</span></span>
