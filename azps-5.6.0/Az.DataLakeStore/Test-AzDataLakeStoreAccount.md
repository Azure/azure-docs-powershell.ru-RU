---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bc8a09add012cb0f190922777e2e9e7fcc46feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995574"
---
# <span data-ttu-id="4cef4-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4cef4-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="4cef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cef4-102">SYNOPSIS</span></span>
<span data-ttu-id="4cef4-103">Проверяет наличие учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4cef4-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="4cef4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4cef4-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cef4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cef4-105">DESCRIPTION</span></span>
<span data-ttu-id="4cef4-106">**Cmdlet Test-AzDataLakeStoreAccount** проверяет наличие учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4cef4-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="4cef4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4cef4-107">EXAMPLES</span></span>

### <span data-ttu-id="4cef4-108">Пример 1. Проверка учетной записи</span><span class="sxs-lookup"><span data-stu-id="4cef4-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="4cef4-109">Эта команда проверяет, существует ли учетная запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="4cef4-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="4cef4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cef4-110">PARAMETERS</span></span>

### <span data-ttu-id="4cef4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cef4-111">-DefaultProfile</span></span>
<span data-ttu-id="4cef4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4cef4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cef4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4cef4-113">-Name</span></span>
<span data-ttu-id="4cef4-114">Указывает имя проверяемой учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4cef4-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="4cef4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cef4-115">-ResourceGroupName</span></span>
<span data-ttu-id="4cef4-116">Имя группы ресурсов, которая содержит проверяемую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4cef4-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="4cef4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cef4-117">CommonParameters</span></span>
<span data-ttu-id="4cef4-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cef4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cef4-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cef4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cef4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cef4-120">INPUTS</span></span>

### <span data-ttu-id="4cef4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4cef4-121">System.String</span></span>

## <span data-ttu-id="4cef4-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4cef4-122">OUTPUTS</span></span>

### <span data-ttu-id="4cef4-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cef4-123">System.Boolean</span></span>

## <span data-ttu-id="4cef4-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4cef4-124">NOTES</span></span>

## <span data-ttu-id="4cef4-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cef4-125">RELATED LINKS</span></span>

[<span data-ttu-id="4cef4-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4cef4-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4cef4-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4cef4-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4cef4-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4cef4-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4cef4-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4cef4-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


