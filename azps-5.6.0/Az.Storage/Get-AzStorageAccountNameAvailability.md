---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 6e4582a8963f3d57bacd3dfb9c869368986c5668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002776"
---
# <span data-ttu-id="5b584-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5b584-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="5b584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b584-102">SYNOPSIS</span></span>
<span data-ttu-id="5b584-103">Проверяет доступность имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5b584-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="5b584-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b584-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b584-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b584-105">DESCRIPTION</span></span>
<span data-ttu-id="5b584-106">Cmdlet **Get-AzStorageAccountNameAvailability** проверяет, допустимо ли имя учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5b584-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="5b584-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b584-107">EXAMPLES</span></span>

### <span data-ttu-id="5b584-108">Пример 1. Проверка доступности имени учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="5b584-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="5b584-109">Эта команда проверяет доступность имени ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="5b584-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="5b584-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b584-110">PARAMETERS</span></span>

### <span data-ttu-id="5b584-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b584-111">-DefaultProfile</span></span>
<span data-ttu-id="5b584-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b584-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b584-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5b584-113">-Name</span></span>
<span data-ttu-id="5b584-114">Указывает имя учетной записи хранения, которую проверяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b584-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b584-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b584-115">CommonParameters</span></span>
<span data-ttu-id="5b584-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b584-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b584-117">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b584-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b584-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b584-118">INPUTS</span></span>

### <span data-ttu-id="5b584-119">System.String</span><span class="sxs-lookup"><span data-stu-id="5b584-119">System.String</span></span>

## <span data-ttu-id="5b584-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b584-120">OUTPUTS</span></span>

### <span data-ttu-id="5b584-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="5b584-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="5b584-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b584-122">NOTES</span></span>

## <span data-ttu-id="5b584-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b584-123">RELATED LINKS</span></span>

[<span data-ttu-id="5b584-124">Azure Storage Manager Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5b584-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


