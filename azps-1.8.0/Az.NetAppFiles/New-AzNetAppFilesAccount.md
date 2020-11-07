---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730776"
---
# <span data-ttu-id="3c4d1-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3c4d1-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="3c4d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4d1-103">Создание новой учетной записи NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="3c4d1-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="3c4d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c4d1-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c4d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="3c4d1-106">Командлет **New-AzNetAppFilesAccount** создает учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="3c4d1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c4d1-107">EXAMPLES</span></span>

### <span data-ttu-id="3c4d1-108">Пример 1: создание учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="3c4d1-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="3c4d1-109">Эта команда создает новую учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="3c4d1-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="3c4d1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c4d1-110">PARAMETERS</span></span>

### <span data-ttu-id="3c4d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4d1-111">-DefaultProfile</span></span>
<span data-ttu-id="3c4d1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c4d1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="3c4d1-113">-Location</span></span>
<span data-ttu-id="3c4d1-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-114">The location of the resource</span></span>

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

### <span data-ttu-id="3c4d1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c4d1-115">-Name</span></span>
<span data-ttu-id="3c4d1-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="3c4d1-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="3c4d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c4d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c4d1-118">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="3c4d1-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3c4d1-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="3c4d1-119">-Tag</span></span>
<span data-ttu-id="3c4d1-120">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="3c4d1-120">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="3c4d1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c4d1-121">-Confirm</span></span>
<span data-ttu-id="3c4d1-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c4d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c4d1-123">-WhatIf</span></span>
<span data-ttu-id="3c4d1-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c4d1-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c4d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4d1-126">CommonParameters</span></span>
<span data-ttu-id="3c4d1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c4d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3c4d1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c4d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4d1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c4d1-129">INPUTS</span></span>

### <span data-ttu-id="3c4d1-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3c4d1-130">None</span></span>

## <span data-ttu-id="3c4d1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c4d1-131">OUTPUTS</span></span>

### <span data-ttu-id="3c4d1-132">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3c4d1-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="3c4d1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c4d1-133">NOTES</span></span>

## <span data-ttu-id="3c4d1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c4d1-134">RELATED LINKS</span></span>
