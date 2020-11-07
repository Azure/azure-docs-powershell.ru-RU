---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901577"
---
# <span data-ttu-id="4e835-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e835-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="4e835-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e835-102">SYNOPSIS</span></span>
<span data-ttu-id="4e835-103">Настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="4e835-103">Configures an API management group.</span></span>

## <span data-ttu-id="4e835-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e835-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e835-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e835-105">DESCRIPTION</span></span>
<span data-ttu-id="4e835-106">Командлет **Set-AzApiManagementGroup** настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="4e835-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="4e835-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e835-107">EXAMPLES</span></span>

### <span data-ttu-id="4e835-108">Пример 1: Настройка группы управления</span><span class="sxs-lookup"><span data-stu-id="4e835-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="4e835-109">Эта команда настраивает группу управления с именем Group0001.</span><span class="sxs-lookup"><span data-stu-id="4e835-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="4e835-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e835-110">PARAMETERS</span></span>

### <span data-ttu-id="4e835-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4e835-111">-Context</span></span>
<span data-ttu-id="4e835-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4e835-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e835-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e835-113">-DefaultProfile</span></span>
<span data-ttu-id="4e835-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e835-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e835-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="4e835-115">-Description</span></span>
<span data-ttu-id="4e835-116">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="4e835-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e835-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4e835-117">-GroupId</span></span>
<span data-ttu-id="4e835-118">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="4e835-118">Specifies the identifier of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e835-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e835-119">-Name</span></span>
<span data-ttu-id="4e835-120">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="4e835-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e835-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e835-121">-PassThru</span></span>
<span data-ttu-id="4e835-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="4e835-122">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e835-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e835-123">CommonParameters</span></span>
<span data-ttu-id="4e835-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e835-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e835-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e835-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e835-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e835-126">INPUTS</span></span>

### <span data-ttu-id="4e835-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4e835-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4e835-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4e835-128">System.String</span></span>

### <span data-ttu-id="4e835-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4e835-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4e835-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e835-130">OUTPUTS</span></span>

### <span data-ttu-id="4e835-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e835-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="4e835-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e835-132">NOTES</span></span>

## <span data-ttu-id="4e835-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e835-133">RELATED LINKS</span></span>

[<span data-ttu-id="4e835-134">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e835-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="4e835-135">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e835-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="4e835-136">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="4e835-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


