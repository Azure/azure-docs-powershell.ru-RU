---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315470"
---
# <span data-ttu-id="74ead-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="74ead-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="74ead-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74ead-102">SYNOPSIS</span></span>
<span data-ttu-id="74ead-103">Добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="74ead-103">Adds a user to a group.</span></span>

## <span data-ttu-id="74ead-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74ead-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74ead-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74ead-105">DESCRIPTION</span></span>
<span data-ttu-id="74ead-106">Командлет **Add-AzApiManagementUserToGroup** добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="74ead-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="74ead-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74ead-107">EXAMPLES</span></span>

### <span data-ttu-id="74ead-108">Пример 1: Добавление пользователя в группу</span><span class="sxs-lookup"><span data-stu-id="74ead-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="74ead-109">Эта команда добавляет существующего пользователя в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="74ead-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="74ead-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74ead-110">PARAMETERS</span></span>

### <span data-ttu-id="74ead-111">-Context</span><span class="sxs-lookup"><span data-stu-id="74ead-111">-Context</span></span>
<span data-ttu-id="74ead-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="74ead-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="74ead-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74ead-113">This parameter is required.</span></span>

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

### <span data-ttu-id="74ead-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ead-114">-DefaultProfile</span></span>
<span data-ttu-id="74ead-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74ead-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ead-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="74ead-116">-GroupId</span></span>
<span data-ttu-id="74ead-117">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="74ead-117">Specifies the group ID.</span></span>
<span data-ttu-id="74ead-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74ead-118">This parameter is required.</span></span>

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

### <span data-ttu-id="74ead-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74ead-119">-PassThru</span></span>
<span data-ttu-id="74ead-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="74ead-120">passthru</span></span>

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

### <span data-ttu-id="74ead-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="74ead-121">-UserId</span></span>
<span data-ttu-id="74ead-122">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="74ead-122">Specifies the user ID.</span></span>
<span data-ttu-id="74ead-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74ead-123">This parameter is required.</span></span>

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

### <span data-ttu-id="74ead-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ead-124">CommonParameters</span></span>
<span data-ttu-id="74ead-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74ead-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ead-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74ead-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ead-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74ead-127">INPUTS</span></span>

### <span data-ttu-id="74ead-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="74ead-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74ead-129">System. String</span><span class="sxs-lookup"><span data-stu-id="74ead-129">System.String</span></span>

### <span data-ttu-id="74ead-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74ead-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74ead-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74ead-131">OUTPUTS</span></span>

### <span data-ttu-id="74ead-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74ead-132">System.Boolean</span></span>

## <span data-ttu-id="74ead-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="74ead-133">NOTES</span></span>

## <span data-ttu-id="74ead-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74ead-134">RELATED LINKS</span></span>

[<span data-ttu-id="74ead-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74ead-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="74ead-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="74ead-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


