---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733412"
---
# <span data-ttu-id="a7bf0-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="a7bf0-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="a7bf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bf0-103">Удаление пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7bf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7bf0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7bf0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="a7bf0-106">Командлет **Remove-AzureRmApiManagementUserFromGroup** удаляет пользователя из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="a7bf0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7bf0-107">EXAMPLES</span></span>

### <span data-ttu-id="a7bf0-108">Пример 1: Удаление пользователя из группы</span><span class="sxs-lookup"><span data-stu-id="a7bf0-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="a7bf0-109">Эта команда удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="a7bf0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7bf0-110">PARAMETERS</span></span>

### <span data-ttu-id="a7bf0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a7bf0-111">-Context</span></span>
<span data-ttu-id="a7bf0-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a7bf0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a7bf0-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a7bf0-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a7bf0-114">-GroupId</span></span>
<span data-ttu-id="a7bf0-115">Указывает идентификатор группы, из которой нужно удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="a7bf0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7bf0-116">-PassThru</span></span>
<span data-ttu-id="a7bf0-117">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="a7bf0-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="a7bf0-118">-UserId</span></span>
<span data-ttu-id="a7bf0-119">Указывает идентификатор пользователя, который нужно удалить из группы.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="a7bf0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bf0-120">-DefaultProfile</span></span>
<span data-ttu-id="a7bf0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7bf0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bf0-122">CommonParameters</span></span>
<span data-ttu-id="a7bf0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7bf0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bf0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7bf0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bf0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7bf0-125">INPUTS</span></span>

## <span data-ttu-id="a7bf0-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7bf0-126">OUTPUTS</span></span>

### <span data-ttu-id="a7bf0-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7bf0-127">System.Boolean</span></span>

## <span data-ttu-id="a7bf0-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7bf0-128">NOTES</span></span>

## <span data-ttu-id="a7bf0-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7bf0-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7bf0-130">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="a7bf0-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="a7bf0-131">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a7bf0-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


