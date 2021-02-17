---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215865"
---
# <span data-ttu-id="167f7-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="167f7-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="167f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="167f7-102">SYNOPSIS</span></span>
<span data-ttu-id="167f7-103">Получает файл удаленного рабочего стола для экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="167f7-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="167f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="167f7-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="167f7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="167f7-105">DESCRIPTION</span></span>
<span data-ttu-id="167f7-106">Получает файл удаленного рабочего стола для экземпляра роли в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="167f7-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="167f7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="167f7-107">EXAMPLES</span></span>

### <span data-ttu-id="167f7-108">Пример 1. Получить RDP-файл</span><span class="sxs-lookup"><span data-stu-id="167f7-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="167f7-109">Эта команда получает RDP-файл для экземпляра роли ContosoFrontEnd IN 0 облачной службы ContosoCS, которая принадлежит к группе ресурсов \_ \_ ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="167f7-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="167f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="167f7-110">PARAMETERS</span></span>

### <span data-ttu-id="167f7-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="167f7-111">-CloudServiceName</span></span>
<span data-ttu-id="167f7-112">.</span><span class="sxs-lookup"><span data-stu-id="167f7-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167f7-113">-DefaultProfile</span></span>
<span data-ttu-id="167f7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="167f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167f7-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="167f7-115">-OutFile</span></span>
<span data-ttu-id="167f7-116">Путь к записи выходного файла</span><span class="sxs-lookup"><span data-stu-id="167f7-116">Path to write output file to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167f7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="167f7-117">-PassThru</span></span>
<span data-ttu-id="167f7-118">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="167f7-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="167f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="167f7-120">.</span><span class="sxs-lookup"><span data-stu-id="167f7-120">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167f7-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="167f7-121">-RoleInstanceName</span></span>
<span data-ttu-id="167f7-122">Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="167f7-122">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167f7-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="167f7-123">-SubscriptionId</span></span>
<span data-ttu-id="167f7-124">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="167f7-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="167f7-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="167f7-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167f7-126">CommonParameters</span></span>
<span data-ttu-id="167f7-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167f7-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="167f7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167f7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="167f7-129">INPUTS</span></span>

## <span data-ttu-id="167f7-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="167f7-130">OUTPUTS</span></span>

### <span data-ttu-id="167f7-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="167f7-131">System.Boolean</span></span>

## <span data-ttu-id="167f7-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="167f7-132">NOTES</span></span>

<span data-ttu-id="167f7-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="167f7-133">ALIASES</span></span>

## <span data-ttu-id="167f7-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="167f7-134">RELATED LINKS</span></span>

