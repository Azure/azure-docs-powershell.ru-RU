---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246347"
---
# <span data-ttu-id="7274b-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7274b-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="7274b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7274b-102">SYNOPSIS</span></span>
<span data-ttu-id="7274b-103">Возвращает или перечисляет политику репликации объектов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7274b-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="7274b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7274b-104">SYNTAX</span></span>

### <span data-ttu-id="7274b-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7274b-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7274b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7274b-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7274b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7274b-107">DESCRIPTION</span></span>
<span data-ttu-id="7274b-108">Командлет **Get-AzStorageObjectReplicationPolicy** получает или перечисляет политику репликации объектов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7274b-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="7274b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7274b-109">EXAMPLES</span></span>

### <span data-ttu-id="7274b-110">Пример 1: получение политики репликации объектов с определенным идентификатором политики и отображение ее правил.</span><span class="sxs-lookup"><span data-stu-id="7274b-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="7274b-111">Эта команда получает политику репликации объектов с определенным идентификатором политики и отображает ее правила.</span><span class="sxs-lookup"><span data-stu-id="7274b-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="7274b-112">Пример 2: список политики репликации объектов List из учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7274b-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="7274b-113">Эта команда перечисляет политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7274b-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="7274b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7274b-114">PARAMETERS</span></span>

### <span data-ttu-id="7274b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7274b-115">-DefaultProfile</span></span>
<span data-ttu-id="7274b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7274b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7274b-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="7274b-117">-PolicyId</span></span>
<span data-ttu-id="7274b-118">Идентификатор политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="7274b-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7274b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7274b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7274b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7274b-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7274b-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7274b-121">-StorageAccount</span></span>
<span data-ttu-id="7274b-122">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7274b-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7274b-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7274b-123">-StorageAccountName</span></span>
<span data-ttu-id="7274b-124">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7274b-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7274b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7274b-125">CommonParameters</span></span>
<span data-ttu-id="7274b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7274b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7274b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7274b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7274b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7274b-128">INPUTS</span></span>

### <span data-ttu-id="7274b-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7274b-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7274b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7274b-130">OUTPUTS</span></span>

### <span data-ttu-id="7274b-131">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7274b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="7274b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="7274b-132">NOTES</span></span>

## <span data-ttu-id="7274b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7274b-133">RELATED LINKS</span></span>
