---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: abf9cab8e7e832a6221a25aff40f4d7b7ae55d58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733505"
---
# <span data-ttu-id="d7dfb-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="d7dfb-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="d7dfb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dfb-103">Удаление пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7dfb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7dfb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7dfb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="d7dfb-106">Командлет **Remove-AzureRmApiManagementUserFromGroup** удаляет пользователя из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="d7dfb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="d7dfb-108">Пример 1: Удаление пользователя из группы</span><span class="sxs-lookup"><span data-stu-id="d7dfb-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="d7dfb-109">Эта команда удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="d7dfb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7dfb-110">PARAMETERS</span></span>

### <span data-ttu-id="d7dfb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d7dfb-111">-Context</span></span>
<span data-ttu-id="d7dfb-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d7dfb-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d7dfb-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d7dfb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7dfb-114">-DefaultProfile</span></span>
<span data-ttu-id="d7dfb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dfb-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d7dfb-116">-GroupId</span></span>
<span data-ttu-id="d7dfb-117">Указывает идентификатор группы, из которой нужно удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="d7dfb-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7dfb-118">-PassThru</span></span>
<span data-ttu-id="d7dfb-119">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d7dfb-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="d7dfb-120">-UserId</span></span>
<span data-ttu-id="d7dfb-121">Указывает идентификатор пользователя, который нужно удалить из группы.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="d7dfb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dfb-122">CommonParameters</span></span>
<span data-ttu-id="d7dfb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7dfb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dfb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7dfb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dfb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7dfb-125">INPUTS</span></span>

### <span data-ttu-id="d7dfb-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7dfb-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7dfb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d7dfb-127">System.String</span></span>

### <span data-ttu-id="d7dfb-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7dfb-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7dfb-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7dfb-129">OUTPUTS</span></span>

### <span data-ttu-id="d7dfb-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7dfb-130">System.Boolean</span></span>

## <span data-ttu-id="d7dfb-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7dfb-131">NOTES</span></span>

## <span data-ttu-id="d7dfb-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7dfb-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7dfb-133">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="d7dfb-133">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="d7dfb-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d7dfb-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


