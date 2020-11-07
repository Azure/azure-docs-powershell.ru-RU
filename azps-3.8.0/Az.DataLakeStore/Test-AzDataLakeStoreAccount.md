---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913036"
---
# <span data-ttu-id="e0bb8-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0bb8-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e0bb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bb8-103">Проверка наличия учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e0bb8-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e0bb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0bb8-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0bb8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bb8-106">Командлет **Test-AzDataLakeStoreAccount** проверяет наличие учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e0bb8-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e0bb8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="e0bb8-108">Пример 1: Проверка учетной записи</span><span class="sxs-lookup"><span data-stu-id="e0bb8-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e0bb8-109">Эта команда проверяет, существует ли учетная запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="e0bb8-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="e0bb8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0bb8-110">PARAMETERS</span></span>

### <span data-ttu-id="e0bb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bb8-111">-DefaultProfile</span></span>
<span data-ttu-id="e0bb8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e0bb8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0bb8-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0bb8-113">-Name</span></span>
<span data-ttu-id="e0bb8-114">Указывает имя учетной записи Data Lake Store для проверки.</span><span class="sxs-lookup"><span data-stu-id="e0bb8-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0bb8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0bb8-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0bb8-116">Указывает имя группы ресурсов, которая содержит учетную запись для проверки.</span><span class="sxs-lookup"><span data-stu-id="e0bb8-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0bb8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bb8-117">CommonParameters</span></span>
<span data-ttu-id="e0bb8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0bb8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bb8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0bb8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bb8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0bb8-120">INPUTS</span></span>

### <span data-ttu-id="e0bb8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e0bb8-121">System.String</span></span>

## <span data-ttu-id="e0bb8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0bb8-122">OUTPUTS</span></span>

### <span data-ttu-id="e0bb8-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0bb8-123">System.Boolean</span></span>

## <span data-ttu-id="e0bb8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0bb8-124">NOTES</span></span>

## <span data-ttu-id="e0bb8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0bb8-125">RELATED LINKS</span></span>

[<span data-ttu-id="e0bb8-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0bb8-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e0bb8-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0bb8-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e0bb8-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0bb8-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e0bb8-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e0bb8-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


