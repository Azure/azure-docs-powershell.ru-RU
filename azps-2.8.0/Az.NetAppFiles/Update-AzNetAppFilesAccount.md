---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 46415c4d1671c874135b8d754e9217212ade3838
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902601"
---
# <span data-ttu-id="2fdb8-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2fdb8-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="2fdb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fdb8-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdb8-103">Обновляет учетную запись NetApp файлы Azure (ANF) в соответствии с необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="2fdb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fdb8-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="2fdb8-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdb8-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fdb8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdb8-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fdb8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdb8-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fdb8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fdb8-108">DESCRIPTION</span></span>
<span data-ttu-id="2fdb8-109">Командлет **Update-AzNetAppFilesAccount** изменяет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="2fdb8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fdb8-110">EXAMPLES</span></span>

### <span data-ttu-id="2fdb8-111">Пример 1: обновление учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2fdb8-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="2fdb8-112">Эта команда выполняет обновление для указанной учетной записи, изменяя указанные Теги.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="2fdb8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fdb8-113">PARAMETERS</span></span>

### <span data-ttu-id="2fdb8-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="2fdb8-114">-ActiveDirectories</span></span>
<span data-ttu-id="2fdb8-115">Массив хэш-таблиц, который представляет активные каталоги</span><span class="sxs-lookup"><span data-stu-id="2fdb8-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdb8-116">-DefaultProfile</span></span>
<span data-ttu-id="2fdb8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fdb8-118">-InputObject</span></span>
<span data-ttu-id="2fdb8-119">Объект учетной записи для обновления</span><span class="sxs-lookup"><span data-stu-id="2fdb8-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-120">-Location</span><span class="sxs-lookup"><span data-stu-id="2fdb8-120">-Location</span></span>
<span data-ttu-id="2fdb8-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fdb8-122">-Name</span></span>
<span data-ttu-id="2fdb8-123">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2fdb8-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdb8-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fdb8-125">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2fdb8-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fdb8-126">-ResourceId</span></span>
<span data-ttu-id="2fdb8-127">Идентификатор ресурса для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2fdb8-127">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="2fdb8-128">-Tag</span></span>
<span data-ttu-id="2fdb8-129">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="2fdb8-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fdb8-130">-Confirm</span></span>
<span data-ttu-id="2fdb8-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdb8-132">-WhatIf</span></span>
<span data-ttu-id="2fdb8-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fdb8-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdb8-135">CommonParameters</span></span>
<span data-ttu-id="2fdb8-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fdb8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2fdb8-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdb8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdb8-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fdb8-138">INPUTS</span></span>

### <span data-ttu-id="2fdb8-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="2fdb8-139">None</span></span>

## <span data-ttu-id="2fdb8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fdb8-140">OUTPUTS</span></span>

### <span data-ttu-id="2fdb8-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2fdb8-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2fdb8-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fdb8-142">NOTES</span></span>

## <span data-ttu-id="2fdb8-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fdb8-143">RELATED LINKS</span></span>
