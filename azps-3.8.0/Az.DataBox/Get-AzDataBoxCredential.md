---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066644"
---
# <span data-ttu-id="d3344-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="d3344-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="d3344-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3344-102">SYNOPSIS</span></span>
<span data-ttu-id="d3344-103">Получает учетные данные databox для определенного задания.</span><span class="sxs-lookup"><span data-stu-id="d3344-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="d3344-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3344-104">SYNTAX</span></span>

### <span data-ttu-id="d3344-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3344-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3344-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3344-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3344-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3344-107">DESCRIPTION</span></span>
<span data-ttu-id="d3344-108">Командлет **Get-AzDataBoxCredential** возвращает учетные данные databox определенного задания.</span><span class="sxs-lookup"><span data-stu-id="d3344-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="d3344-109">Внутренние свойства возвращаемого объекта учетных данных будут различаться для разных типов SKU.</span><span class="sxs-lookup"><span data-stu-id="d3344-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="d3344-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3344-110">EXAMPLES</span></span>

### <span data-ttu-id="d3344-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3344-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="d3344-112">Это retuns JobSecrets указанного задания</span><span class="sxs-lookup"><span data-stu-id="d3344-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="d3344-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d3344-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="d3344-114">Это retuns JobSecrets указанного задания</span><span class="sxs-lookup"><span data-stu-id="d3344-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="d3344-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3344-115">PARAMETERS</span></span>

### <span data-ttu-id="d3344-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3344-116">-DefaultProfile</span></span>
<span data-ttu-id="d3344-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3344-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3344-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3344-118">-Name</span></span>
<span data-ttu-id="d3344-119">Название задания Databox</span><span class="sxs-lookup"><span data-stu-id="d3344-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3344-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3344-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3344-121">Имя группы ресурсов "работа Databox"</span><span class="sxs-lookup"><span data-stu-id="d3344-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3344-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3344-122">-ResourceId</span></span>
<span data-ttu-id="d3344-123">Код ресурса задания Databox</span><span class="sxs-lookup"><span data-stu-id="d3344-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3344-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3344-124">CommonParameters</span></span>
<span data-ttu-id="d3344-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3344-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3344-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3344-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3344-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3344-127">INPUTS</span></span>

### <span data-ttu-id="d3344-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d3344-128">System.String</span></span>

## <span data-ttu-id="d3344-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3344-129">OUTPUTS</span></span>

### <span data-ttu-id="d3344-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. Models. UnencryptedCredentials, Microsoft. Azure. Management. DataBox, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d3344-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d3344-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3344-131">NOTES</span></span>

## <span data-ttu-id="d3344-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3344-132">RELATED LINKS</span></span>
